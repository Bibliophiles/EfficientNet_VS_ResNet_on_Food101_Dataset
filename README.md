# 🍔 ResNet vs EfficientNet on Food101 Dataset (Feature Extraction)

This project compares two powerful convolutional neural network architectures — **ResNet50** and **EfficientNetB0** — on the **Food101 dataset** using **feature extraction**. The goal was to evaluate which model generalizes better on the complex and fine-grained food classification task.

## 📊 Comparison Table

| Model            | Test Accuracy | Test Loss | Parameters (Approx.) | Number of Epochs |
|------------------|---------------|-----------|------------------------|----------------|
| ResNet50         | 0.8368        |**0.5294** | ~23.5 million          |     5          |
| EfficientNetB0   | **0.8616**    |  0.5465   | **~5.0 million**       |     5          |

## ✅ Summary

- **EfficientNetB0 outperformed ResNet50** in the test accuracy but a little under in the test loss.
- It also required **significantly fewer parameters**, making it a more efficient choice for deployment on resource-constrained devices.
- In the **original Food-101 paper** [Food-101: Mining Discriminative Components with Random Forests](https://data.vision.ee.ethz.ch/cvl/datasets_extra/food-101/static/bossard_eccv14_food-101.pdf), a **Random Forest classifier** achieved **just over 50% accuracy**, while both CNNs used here surpassed **80%** accuracy after training.
- Both models were trained for **just 5 epochs**, yet showed strong generalization — highlighting the strength of **transfer learning** through pretrained CNN backbones.
- This shows the effectiveness of newer architecture design and compound scaling in EfficientNet.
- This validates the power of pretrained CNNs, even when used without fine-tuning, for complex image classification tasks.

## 🛠️ Approach

- Used pretrained weights on ImageNet.
- Removed classifier head and froze convolutional base.
- Added custom classification head for Food101 classes.
- Trained using feature extraction (no fine-tuning).
- Models trained for **5 epochs only**.


## 📁 File Structure

- ├── EfficientNet_VS_ResNet_on_Food101_Dataset.ipynb # Notebook with implementation and results
- ├── README.md # Project documentation


## 📦 Dependencies

Install dependencies using:

```bash
pip install tensorflow tensorflow_hub tf_keras tensorboard matplotlib zipfile
```

## 📚 References
- [Food-101: Mining Discriminative Components with Random Forests](https://data.vision.ee.ethz.ch/cvl/datasets_extra/food-101/static/bossard_eccv14_food-101.pdf)
- [Food-101 Dataset](https://data.vision.ee.ethz.ch/cvl/datasets_extra/food-101/)
- [EfficientNet: Rethinking Model Scaling for Convolutional Neural Networks](https://arxiv.org/abs/1905.11946)
- [Deep Residual Learning for Image Recognition (ResNet)](https://arxiv.org/abs/1512.03385)

## ✉️ Contact

If you have any questions, suggestions, or would like to collaborate, feel free to connect with me:

- 📧 Email: [dennisamematekpor](mailto:dennisamematekpor@gmail.com)
- 💼 LinkedIn: [Dennis Amematekpor ANANE](https://www.linkedin.com/in/dennisamematekpor/)


## 📝 License

This project is licensed under the [MIT License](LICENSE).

