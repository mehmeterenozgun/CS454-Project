# Comparative Analysis of Machine Learning & Deep Learning Methods
**Wine Quality Prediction & MNIST Classification**

---

## 📖 Project Overview

We perform a side-by-side comparison of:
- **Classical tree-based ensembles** (XGBoost, Random Forest)
- **Deep tabular models** (NODE, TabNet)

on two standard benchmarks:
1. **Wine Quality** (7-class, imbalanced tabular data)
2. **MNIST** (10-class, balanced image data flattened to tabular features)

Our goal is to assess accuracy, robustness to imbalance, interpretability, and compute trade-offs.

---

## ⚙️ Installation

    1. **Clone the repo**
$bash
git clone https://github.com/mehmeterenozgun/CS454-Project.git
cd CS454-Project

    2.	Create a virtual environment
python3 -m venv venv
source venv/bin/activate

    3.	Install dependencies
pip install -r requirements.txt

📂 Data Preparation
•	Wine Quality
Download winequality-red.csv and winequality-white.csv into data/wine+quality/.
•	MNIST
Place the raw IDX files under data/mnist-dataset/.
The notebooks use idx2numpy to load them.

    4.Run cells in order
Each notebook (wine_xgboost.ipynb, mnist_node.ipynb, etc.) contains:
•	Data loading & preprocessing
•	Model definition & training
•	Evaluation metrics & visualizations

Model          Wine Quality Acc.  MNIST Acc.
XGBoost        ~67 %              ~97.9 %
Random Forest  ~70 %              ~96.9 %
NODE (tuned)   ~66 %              ~98.0 %
TabNet (tuned) ~61.7 %            ~97.3 %


See each notebook for full classification reports, confusion matrices, and hyperparameter tables.

🔍 Key Findings
•	Tree ensembles excel on small, imbalanced tabular data.
•	Deep tabular architectures (NODE/TabNet) can approach or exceed classical methods on larger/balanced datasets, but require careful tuning.
•	Flat tabular models remain surprisingly competitive when MNIST images are simply flattened.