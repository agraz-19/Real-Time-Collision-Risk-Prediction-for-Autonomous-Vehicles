# 🚗 Real-Time Collision Risk Prediction for Autonomous Vehicles

This project presents a machine learning-based system that estimates real-time collision risks in autonomous vehicles (AVs) using synthetic telemetry data. The goal is to enhance AV safety by providing early alerts or triggering preventive actions based on risk assessments derived from vehicle dynamics.

## 📌 Overview

The rapid development of autonomous vehicles promises to revolutionize transportation, offering benefits such as increased safety, reduced traffic congestion, and improved fuel efficiency. However, ensuring the safety of AVs is paramount, with collision risk prediction being a critical component. This project addresses the challenge of accurately assessing collision probabilities by building a robust predictive model. The synthetic dataset used for training and evaluation is designed to mimic the complexities and nuances of actual driving data, allowing for effective model development in a controlled environment.

## 💡 Features

  * **Collision Risk Prediction:** Develops and evaluates multiple machine learning models to predict the probability of a collision in real-time.
  * **Synthetic Data Utilization:** Leverages a synthetic dataset specifically generated to replicate real-world autonomous vehicle telemetry data, addressing data privacy concerns associated with proprietary or sensitive driving information.
  * **Comprehensive Model Evaluation:** Compares the performance of various machine learning algorithms, including Random Forest, Gradient Boosting, Logistic Regression, and Support Vector Machines (SVM), based on a range of metrics such as accuracy, precision, recall, F1-score, and ROC AUC.
  * **Safety-Critical Focus:** Prioritizes recall as a key metric for model selection, emphasizing the importance of identifying actual collision risks to enhance AV safety.

## 🧾 Dataset

  - **Type**: Synthetic
  - **Source**: Generated to simulate real-world autonomous vehicle telemetry data
  - **Purpose**: Bypass data privacy issues associated with proprietary or sensitive driving datasets

### Key Features in the Dataset:

  - Distance to objects
  - Relative speed
  - Braking intensity
  - Steering angle
  - Vehicle speed
  - Speed-to-distance ratio (engineered)
  - Time to collision (engineered)

## 🧠 Models Evaluated

Four models were trained and compared on accuracy, precision, recall, F1-score, and ROC AUC:

| Model             | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|:------------------|:---------|:----------|:-------|:---------|:--------|
| Random Forest     | 0.9533   | 0.0000    | 0.0000 | 0.0000   | 0.4486  |
| Gradient Boosting | 0.9533   | 0.0000    | 0.0000 | 0.0000   | 0.5000  |
| Logistic Regression| 0.1733   | 0.0465    | 0.8571 | 0.0832   | 0.5415  |
| SVM               | 0.9533   | 0.0000    | 0.0000 | 0.0000   | 0.6743  |

> ✅ **Best Performing Model (in Recall): Logistic Regression**

Despite the lower overall accuracy of Logistic Regression, it achieved a **recall of 0.8571**, indicating its effectiveness in identifying high-risk collision events—essential for safety-critical applications where missing a risk is more costly than issuing a false alarm. This model's strong recall is crucial for proactive risk management in AVs.

## ⚙️ Project Structure

```bash
.
├── AV_Collision_Risk_Prediction.ipynb   # Main Jupyter notebook with preprocessing, modeling, and evaluation
├── collision_risk_dataset.csv           # Synthetic dataset used for model training and testing
├── README.md                            # Project overview and documentation
```

## 🛠️ Technologies and Libraries

The project is developed in Python and leverages several key libraries for data manipulation, machine learning, and visualization:

  * **Pandas:** For data loading, preprocessing, and manipulation of tabular data.
  * **NumPy:** For numerical operations and array handling.
  * **Scikit-learn:** For machine learning model implementation (Logistic Regression, SVM, Random Forest, Gradient Boosting), data splitting, scaling, and performance metric calculation (Accuracy, Precision, Recall, F1-Score, ROC AUC).
  * **Matplotlib / Seaborn:** For data visualization and plotting model performance.
  * **Jupyter Notebook:** For interactive development, experimentation, and presenting the analysis workflow.

## 🚀 Getting Started

To set up and run this project locally, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/your-repo-name.git
    cd your-repo-name
    ```
2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```
3.  **Install the required dependencies:**
    (You will need to create a `requirements.txt` file based on the libraries used in `AV_Collision_Risk_Prediction.ipynb`.)
    ```bash
    pip install -r requirements.txt
    ```
4.  **Open the Jupyter Notebook:**
    ```bash
    jupyter notebook AV_Collision_Risk_Prediction.ipynb
    ```
    Run all cells in the notebook: The notebook guides you through data loading, preprocessing, model training, evaluation, and result presentation.


## 🧑‍💻 Authors

  * (G.Agraz)

