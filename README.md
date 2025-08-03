#  Emotion Detection Chatbot (Keras Model Loader)

This project demonstrates how to load a fully trained Keras model from a `.h5` file and make predictions. The model consists of an Embedding layer, an LSTM layer, and two Dense layers, designed for emotion classification from text inputs.

---
img_path = "Screenshot 2025-08-04 011900.png"
##  Project Structure

Emotion Chatbot/
│
├── train.h5 # Trained Keras model (includes architecture + weights + optimizer state)
├── load_model.py # Python script to load and run the model
├── Screenshot 2025-08-04 011900.png # Output screenshot
└── README.md # Project documentation

yaml
Copy
Edit

---

##  How to Use

### 1. Install Dependencies

Make sure you have Python 3.x installed, then install required packages:

```bash
pip install tensorflow keras numpy
2. Load the Model
Run the script to load the .h5 model and view its architecture:

bash
Copy
Edit
python load_model.py
This will:

Load the model from train.h5

Print the model summary

Run a dummy prediction on a randomly generated input

3. Model Architecture
The loaded model includes:

Embedding Layer

LSTM Layer

Dense Layers (including output for classification)

You can visualize the architecture by viewing the summary in terminal or examining the weights using h5py if needed.

4. Sample Output

 Dummy Prediction Example
The code uses:

python
Copy
Edit
dummy_input = np.random.randint(1, 1000, size=(1, 20))
prediction = model.predict(dummy_input)
It simulates a sequence of tokens for testing purposes.

 Notes
Do not use model.load_weights() unless you manually define the model structure.

Always use keras.models.load_model() when the .h5 file contains both model and weights.

✨ Credits
Created by Sagnik Patra
