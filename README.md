# 🎨 Neural Style Transfer using AdaIN

A deep learning-based **Neural Style Transfer** web application built with **PyTorch** and **Flask**. This project uses **Adaptive Instance Normalization (AdaIN)** to transfer the artistic style of one image onto another while preserving the original content.

---

## 📌 Features

* Upload any content image.
* Upload any style image.
* Adjust the style intensity using the **Alpha** parameter.
* Real-time style transfer through a simple web interface.
* Fast inference using a pretrained AdaIN decoder.
* Supports JPG, JPEG, and PNG images.

---

## 🖼️ How It Works

The project follows the AdaIN pipeline:

1. Extract content and style features using a pretrained **VGG-19 Encoder**.
2. Apply **Adaptive Instance Normalization (AdaIN)** to align the statistics of the content features with the style features.
3. Blend the transformed features using the alpha parameter.
4. Reconstruct the stylized image using a trained Decoder network.

---

## 🛠️ Tech Stack

* Python
* PyTorch
* TorchVision
* Flask
* Flask-WTF
* Bootstrap
* Pillow

---

## 📂 Project Structure

```text
.
├── app.py
├── requirements.txt
├── utils/
│   ├── model.py
│   └── utils.py
├── templates/
│   └── index.html
├── static/
│   └── uploads/
├── experiment/
├── vgg_normalised.pth
└── README.md
```

---

## 🚀 Installation

Clone the repository:

```bash
git clone <repository-url>
cd <repository-folder>
```

Create a virtual environment:

```bash
python -m venv venvadain
```

Activate it:

**Windows**

```bash
venvadain\Scripts\activate
```

**Linux / macOS**

```bash
source venvadain/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Application

Start the Flask server:

```bash
python app.py
```

Open your browser and visit:

```text
http://localhost:5000
```

---

## 📖 Usage

1. Upload a **Content Image**.
2. Upload a **Style Image**.
3. Set the **Alpha** value (0–1).
4. Click **Transfer Style**.
5. Download or view the generated stylized image.

---

## 📸 Example Workflow

```text
Content Image
       +
Style Image
       │
       ▼
 VGG Encoder
       │
       ▼
Adaptive Instance Normalization (AdaIN)
       │
       ▼
 Decoder Network
       │
       ▼
 Stylized Output
```

---

## 📚 Model Architecture

* **Encoder:** Pretrained VGG-19 (up to ReLU4_1)
* **Feature Alignment:** Adaptive Instance Normalization (AdaIN)
* **Decoder:** Convolutional Decoder Network
* **Framework:** PyTorch


