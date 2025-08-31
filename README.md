# 🌾 GrainPalette — Rice Type Classification with Transfer Learning

GrainPalette is a deep learning project that classifies **five types of rice grains** using **Convolutional Neural Networks (CNN)** and **Transfer Learning (MobileNetV2)**. The trained model is deployed as a **Flask web app**, allowing users to upload rice grain images and get predictions instantly.

---

## 🚀 Features

* 📷 Upload an image of a rice grain and get classification results.
* 🧠 Transfer learning with **MobileNetV2** for lightweight, high-accuracy predictions.
* 🌐 Flask-based web interface for easy use.
* 👩‍🌾 Use cases for **farmers, researchers, and home growers**.

---

## 📂 Project Structure

```
GrainPalette/
├─ app/
│  ├─ static/              # CSS, JS, images
│  ├─ templates/           # HTML files (Flask Jinja2)
│  └─ app.py               # Flask backend
├─ data/
│  ├─ train/               # training images (one folder per class)
│  ├─ val/                 # validation images
│  └─ test/                # test images
├─ models/
│  ├─ rice_mnv2.h5         # trained model
│  └─ class_indices.json   # mapping class → label
├─ src/
│  ├─ train.py             # model training script
│  ├─ predict.py           # CLI prediction
│  └─ utils.py             # helper functions
├─ notebooks/
│  └─ train.ipynb          # Jupyter notebook version of training
├─ requirements.txt
└─ README.md
```

---

## ⚙️ Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/grainpalette.git
   cd grainpalette
   ```

2. Create a conda environment:

   ```bash
   conda create -n grainpalette python=3.8 -y
   conda activate grainpalette
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

---

## 🏋️ Training the Model

Ensure your dataset is inside the `data/` folder (train/val/test subfolders).

Run training script:

```bash
python src/train.py --epochs 10 --batch_size 32 --lr 0.0001
```

This will generate:

* `models/rice_mnv2.h5` (trained model)
* `models/class_indices.json` (label mappings)

---

## 🌐 Running the Flask App

After training, launch the Flask web app:

```bash
cd app
python app.py
```

Visit: **[http://127.0.0.1:5000/](http://127.0.0.1:5000/)**

Upload an image and view predictions on the browser.

---

## 📊 Example Use Cases

* 👨‍🌾 **Farmers**: Identify seed varieties before cultivation.
* 🔬 **Researchers**: Classify samples during trials.
* 🏡 **Home growers**: Learn about rice biodiversity.

---

## 📦 Requirements

* Python 3.8+
* TensorFlow 2.3.2
* Flask 2.0.3
* NumPy, Pandas, Matplotlib, scikit-learn, Pillow, tqdm

Install via:

```bash
pip install -r requirements.txt
```

---

## 📜 License

This project is licensed under the MIT License.

---

## 🤝 Contributing

Pull requests are welcome! If you’d like to add improvements (UI, datasets, performance tweaks), fork the repo and submit a PR.

---

## 🙌 Acknowledgements

* [TensorFlow](https://www.tensorflow.org/)
* [MobileNetV2](https://arxiv.org/abs/1801.04381)
* [Flask](https://flask.palletsprojects.com/)

---

🌾 *GrainPalette: Empowering Agriculture through AI*
