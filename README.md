
# Speech Emotion Recognition using CNN-LSTM

## 📌 Project Overview
This project implements a **Speech Emotion Recognition** system using a **CNN-LSTM** deep learning model. It classifies emotions from speech using features like **MFCCs, Chromagrams, Spectral Contrast, and Log-Mel Spectrograms**. The model is trained on the **RAVDESS dataset** and achieves high accuracy in distinguishing six emotions: **calm, happy, fearful, disgust, angry, and sad**.

## 🚀 Features
- **Deep Learning Architecture:** Uses a hybrid CNN-LSTM model for feature extraction and sequence learning.
- **Data Augmentation:** Applies pitch shifting, time-stretching, and noise addition.
- **Class Balancing:** Computes class weights for handling imbalanced datasets.
- **Performance Analysis:** Plots training curves and fits polynomial functions for evaluation.

---

## 🛠 Installation
### Clone the repository:
```bash
git clone https://github.com/YOUR_USERNAME/Speech-Emotion-Recognition.git
cd Speech-Emotion-Recognition
```

### Install dependencies:
```bash
pip install -r requirements.txt
```

---

## 📂 Dataset
This project uses the **RAVDESS** dataset. Download it from [here](https://zenodo.org/record/1188976) and place the files inside the `data/` directory.

### Expected Structure:
```
Speech-Emotion-Recognition/
├── data/
│   ├── Actor_01/
│   ├── Actor_02/
│   ├── ...
│   ├── Actor_24/
```

---

## 🔥 Model Training
To train the model, run:
```bash
python train_model.py
```

---

## 📊 Model Evaluation
To evaluate the trained model:
```bash
python evaluate_model.py
```

---

## 🎤 Real-Time Inference
To classify a new audio file:
```bash
python inference.py --file path/to/audio.wav
```

---

## 📈 Results & Analysis
The model achieved **77.78% test accuracy**. Below are the polynomial fit coefficients for accuracy and loss curves:
- **Train Accuracy Polynomial Coefficients:** `[-0.00095, 0.05072, 0.24348]`
- **Validation Accuracy Polynomial Coefficients:** `[-0.00076, 0.03725, 0.32575]`
- **Train Loss Polynomial Coefficients:** `[0.00177, -0.10556, 1.75750]`
- **Validation Loss Polynomial Coefficients:** `[0.00186, -0.08116, 1.61029]`

---

## 📌 Conclusion
The CNN-LSTM model effectively classifies emotions with **high accuracy**. However, fine-tuning hyperparameters and using a **larger dataset** can further improve performance. The model performed comparably to **DataFlair's implementation** while using **enhanced feature extraction** and **data augmentation techniques**.

---

## 💡 Future Work
- Implement real-time emotion detection.
- Expand dataset for better generalization.
- Experiment with Transformer-based architectures.

---

## 👨‍💻 Author
**[Your Name]**  
LinkedIn: [Your LinkedIn](https://www.linkedin.com/in/YOUR_PROFILE/)  
GitHub: [Your GitHub](https://github.com/YOUR_USERNAME)

---

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

