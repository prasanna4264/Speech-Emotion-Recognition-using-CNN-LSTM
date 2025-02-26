
# Speech Emotion Recognition using CNN-LSTM

## Project Overview
This project implements a **Speech Emotion Recognition** system using a **CNN-LSTM** deep learning model. It classifies emotions from speech using features like **MFCCs, Chromagrams, Spectral Contrast, and Log-Mel Spectrograms**. The model is trained on the **RAVDESS dataset** and achieves high accuracy in distinguishing six emotions: **calm, happy, fearful, disgust, angry, and sad**.

**Key Steps:**

1. **Data Processing & Augmentation:**
- Used the RAVDESS dataset, which contains emotional speech recordings.
- Implemented data augmentation (time-stretching, pitch shifting, and adding noise) to enhance model generalization.
- Extracted multiple features like MFCCs, Delta MFCCs, Chroma, Spectral Contrast, and Log-Mel Spectrogram.
2. **Feature Engineering & Preprocessing:**
- Standardized features using z-score normalization.
- Encoded emotion labels and converted them into one-hot vectors.
- Handled imbalanced data by computing class weights.
3. **Model Architecture:**
- CNN layers for spatial feature extraction from audio sequences.
- LSTM layers to capture temporal dependencies in speech.
- Fully connected dense layers with dropout for classification.
4. **Training & Optimization:**
- Used cross-entropy loss and Adam optimizer (with reduced learning rate for stability).
- Implemented early stopping and learning rate reduction on plateau to prevent overfitting.
- Achieved ~80% accuracy on the test set.
5. **Deployment & Visualization:**
- Saved the model for future use.
- Visualized training loss & accuracy over epochs.

**Train Accuracy Polynomial:** $y = -0.00095433x^2 + 0.05072405x + 0.2434834$

- The accuracy curve is concave down, meaning the model initially improves but eventually plateaus or slightly decreases, possibly due to overfitting.
- The accuracy is increasing overall but at a slowing rate.
- The initial training accuracy is ~24%.

**Validation Accuracy Polynomial:** $y = -0.00075894x^2 + 0.03725086x + 0.32575878$

- Similar to train accuracy, the validation accuracy curve is concave down but less steep, indicating that performance stabilizes rather than dropping significantly.
- The validation accuracy is increasing at a slightly lower rate than training accuracy.
- The initial validation accuracy is ~32.6%, slightly higher than training accuracy.

**Train Loss Polynomial:** $y = 0.00177142x^2 - 0.10556431x + 1.75750506$

- The loss curve is concave up, meaning after some epochs, the training loss stops decreasing and starts increasing slightly—this can be a sign of overfitting.
- Negative linear term indicates that the loss initially decreases.
- The initial training loss ~1.76.

**Validation Loss Polynomial:** $y = 0.00186634x^2 - 0.08116396x + 1.61029363$

- Concave up, meaning that validation loss initially decreases but then starts increasing again, suggesting potential overfitting.
- The validation loss initially decreases but at a slower rate than training loss.
- The initial validation loss is slightly lower than training loss at ~1.6.

**Conclusion:**

The CNN-LSTM model trained for speech emotion recognition achieved a final test accuracy of **~80%**, with a training accuracy of **~95%** and a validation accuracy of **~80%**. This suggests that while the model generalizes well, there is a small performance gap between training and validation, indicating some overfitting. 

This project demonstrates the effectiveness of deep learning for speech-based emotion recognition, showcasing improvements over existing approaches.

## 📂 Dataset
This project uses the **RAVDESS** dataset. Download it from https://zenodo.org/record/1188976.

## 💡 Future Work
- Implement real-time emotion detection.
- Expand dataset for better generalization.
- Experiment with Transformer-based architectures.

---

## 👨‍💻 Author
**Prasanna Adhikari**  
GitHub: [Your GitHub](https://github.com/prasanna4264)

---

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

