
# 🧘‍♀️ Yoga Pose Feature Extraction

## 📄 Overview

Key functionalities include:

* 🤖 **Pose Estimation** – Use PoseNet/MediaPipe to detect human keypoints (joints, limbs).
* 📐 **Angle-Based Feature Extraction** – Compute joint angles (elbow, knee, shoulder, etc.) for each frame.
* 📊 **Feature Vector Generation** – Prepare angle sets for each frame for model input.
* 💾 **Data Export** – Save features (e.g., in CSV) for training classification or regression models.
* 🧩 **Modular Design** – Clear separation of estimation, feature extraction, and data management modules.

This repo is ideal for anyone building **AI-driven yoga assistants**, fitness trackers, or classification systems using pose-based features.
<p align="center">
  <img src="https://static1.squarespace.com/static/61d3cc4a960d41134f9099d7/61dcce661002a946fb3df95e/61dcce7d1002a946fb3e5d34/1651563384845/tumblr_inline_nzgp24WS8P1rjic88_500.gif?format=1500w" 
       alt="Yoga Pose Animation" 
       width="300" 
       style="border-radius: 10px;" />
</p>


---

## 🚀 Features & Characteristics

| Feature                      | Description                                                           |
| ---------------------------- | --------------------------------------------------------------------- |
| 🎯 Pose Estimation           | Detect 17+ keypoints per frame via PoseNet/MediaPipe.                 |
| 📐 Angle Computation         | Calculate angles between limbs (e.g., knee, elbow, shoulder angles).  |
| 🧠 Feature Extraction Module | Encapsulates logic for angle calculation and normalization.           |
| 📂 Dataset Preparation       | Compute & store feature vectors for each detected frame.              |
| 🛠️ Modular Structure        | Separate scripts for pose extraction, angle logic, and data handling. |
| 🛡 Quality Control           | Handle missing keypoints; clean inaccurate data entries.              |

---

## 📁 Folder Structure

```plaintext
Yoga‑Pose‑Feature‑Extraction/
├── src/
│   ├── pose_estimation.py        # Wraps PoseNet/MediaPipe inference
│   ├── angle_features.py         # Contains functions to compute joint angles
│   └── data_export.py            # Exports frames → angle CSV or JSON
├── data/
│   ├── raw/                      # Input videos or image collections
│   └── processed/                # CSV or JSON of computed features
├── notebooks/
│   └── analysis.ipynb            # Exploratory data analysis on angle features
├── requirements.txt             # Python dependencies
└── README.md
```

---

## 🛠️ Installation

1. **Clone the repo**

   ```bash
   git clone https://github.com/Madhu1207-coder/Yoga-Pose-Feature-Extraction.git
   cd Yoga-Pose-Feature-Extraction
   ```

2. **Set up virtual environment (recommended)**

   ```bash
   python3 -m venv venv
   source venv/bin/activate      # Windows: venv\Scripts\activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

---

## ⚙️ Usage

1. **Prepare your data**
   Place yoga videos or image folders under `data/raw/`

2. **Run pose estimation & feature extraction**

   ```bash
   python src/pose_estimation.py --input data/raw/ --output tmp/keypoints.json
   python src/angle_features.py --keypoints tmp/keypoints.json --output data/processed/angles.csv
   ```

3. **Analyze features**
   Use the notebook to explore distribution of angles across yoga poses.

4. **Use with ML models**
   Train classification/regression models on the feature CSV (e.g., pose recognition).

---

## 📊 Example Output

* `keypoints.json`: contains frame-wise lists of detected (x, y) coordinates.
* `angles.csv`: rows with computed joint angles per frame — ready for ML pipelines.


### 📓 Output – Yoga Pose Feature Extraction

<p align="center">
  <a href="https://github.com/Madhu1207-coder/Yoga-Pose-Feature-Extraction/blob/main/yoga%20pose/yoga-pose-feature-extraction.ipynb">
    <img src="https://img.shields.io/badge/Open%20Notebook-Yoga%20Pose%20Feature%20Extraction-blue?style=for-the-badge&logo=jupyter" alt="Open Notebook">
  </a>
</p>

📘 **Click the badge above to view the full Jupyter Notebook.**

> 💡 For a better preview experience, open it in **[nbviewer](https://nbviewer.org/)**:

```markdown
🔍 [View in nbviewer](https://nbviewer.org/github/Madhu1207-coder/Yoga-Pose-Feature-Extraction/blob/main/yoga%20pose/yoga-pose-feature-extraction.ipynb)
```


## ✅ Use Case Scenarios

* **Pose Classification**: Using angle data to determine which yoga asana is being performed.
* **Fitness App Development**: Build feedback loops based on ideal joint alignments.
* **Research**: Analyze posture consistency or correctness across users or exercises.

---

📄 Author
<table> <tr> <td width="150"><strong>Name</strong></td> <td>: Madhumitha B</td> </tr> <tr> <td><strong>🎓 Role</strong></td> <td>: Aspiring AI & DS Engineer</td> </tr> <tr> <td><strong>🔗 Portfolio</strong></td> <td>: <a href="https://sites.google.com/view/madhumitha-b/project-page" target="_blank">View My Website</a></td> </tr> <tr> <td><strong>📧 Email</strong></td> <td>: <a href="mailto:Madhumithab1207@gmail.com">Madhumithab1207@gmail.com</a></td> </tr> </table>



## 📜 License

Licensed under the **MIT License** (see `LICENSE` file).



## 🌟 Contributing

Contributions are welcome! Here’s how you can help:

1. ⭐ Star the repo
2. Fork → feature-branch → Pull request
3. Describe your feature or fix clearly
4. I may reach out for clarifications or improvements

🙏 Thank You!
<p align="center"> <img src="https://mir-s3-cdn-cf.behance.net/project_modules/fs/a2418f60390643.5a4b910e63f83.gif" width="250" style="border-radius: 50%;" alt="Thank You GIF"/> </p>


