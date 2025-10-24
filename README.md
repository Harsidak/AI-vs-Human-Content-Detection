🧠 Human vs AI Text Classifier (98.9% Accuracy)
🚀 Mission Objective:
Develop a deep learning model capable of distinguishing between human-generated and AI-generated text with extreme precision — achieving a final test accuracy of 98.9%.

📊 Dataset Intel
Source: Kaggle Public Dataset (Human vs AI Text Classification)
Composition:

Human-generated text: ~308,000 samples
AI-generated text: ~181,000 samples
Balancing Strategy:

To prevent bias, the dataset was equalised in two distinct patterns:

Model-1: First 181,000 human samples
Model-2: Last 181,000 human samples

Each subset was paired with all AI samples → trained separately → later evaluated for ensemble potential.

⚙️ Preprocessing Protocol
1) Text Cleaning: Lowercasing, punctuation & digit removal.
2) Stopword Removal using nltk.
3) Tokenisation & Padding via Keras Tokeniser.

Data Split: 80% Training / 20% Validation using stratified sampling.

🧩 Model Architecture
Framework: TensorFlow / Keras
Model Type: Sequential Neural Network

Layers:
Embedding → LSTM (128 units) → Dense (64, relu) → Dropout(0.5) → Dense (1, sigmoid)

Key Training Parameters:

Optimizer: Adam(learning_rate=0.001)
Loss: binary_crossentropy

Epochs: 6
Batch Size: 32
Validation Split: 0.2
GPU Acceleration: Enabled (cuDNN LSTM)

🧠 Results(values are approx and can vary after running the notebook again)
Accuracy Model-1: 98.7% 
Accuracy Model-2: 98.9%

🔥 Highlights

Achieved near-perfect classification between human and AI text.
Balanced dataset strategy prevented bias.
Training is stable under GPU acceleration.
Deployable via .keras model export.
