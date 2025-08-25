# Customer Segmentation using Unsupervised Learning

## 1. Project Overview

This project applies unsupervised machine learning techniques to segment a dataset of insurance policyholders. The primary objective is to transform raw customer data into actionable business intelligence by identifying distinct customer groups based on shared characteristics. By leveraging **K-Means clustering** and **Principal Component Analysis (PCA)**, this analysis provides a data-driven framework for developing targeted marketing strategies, improving customer retention, and informing product development.

---

## 2. Methodology

The analysis was conducted entirely in a Jupyter Notebook (`customer_segmentation_analysis.ipynb`) using Python and a suite of data science libraries.

* **Data Source:** An anonymized insurance dataset sourced from a public repository.
* **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn.
* **Workflow:**
    1.  **Data Cleaning & EDA:** The dataset was loaded, inspected for quality, and explored to understand the distribution and correlation of key features like `age`, `bmi`, and `charges`.
    2.  **Feature Preprocessing:** Categorical features (e.g., `sex`, `smoker`) were one-hot encoded, and all numerical features were standardized using `StandardScaler` to prepare the data for the distance-based clustering algorithm.
    3.  **Dimensionality Reduction:** PCA was used to reduce the feature space to two principal components, enabling effective visualization of the customer segments.
    4.  **Model Development:** The **Elbow Method** was used to determine the optimal number of clusters for the K-Means algorithm. A final model was then trained to segment the customers.
    5.  **Cluster Profiling:** The resulting cluster labels were mapped back to the original data to analyze the mean characteristics of each segment, allowing for the creation of detailed customer personas.

---

## 3. Key Findings: Customer Personas

The analysis successfully identified four distinct customer segments:

* **Cluster 0: Low-Cost, Healthy Non-Smokers:** This is the largest segment, characterized by the lowest average insurance charges. They are non-smokers with a moderate BMI and represent a low-risk, high-value customer base.
* **Cluster 1: High-Cost, High-Risk Smokers:** This group has the highest average insurance charges by a significant margin. They are predominantly smokers, often with a higher BMI, representing a high-risk, high-cost segment.
* **Cluster 2: Mid-Cost, Mid-Risk Individuals:** This segment has moderate insurance charges. They are older on average and have a higher BMI but are non-smokers. They represent a stable, predictable customer group.
* **Cluster 3: Young, Healthy Individuals:** This group consists of the youngest customers with the lowest average BMI and number of children. Their insurance charges are relatively low, making them a key target for long-term customer value.

---

## 4. How to Run This Project

To replicate this analysis, please follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/priyam0k/insurance-customer-segmentation.git](https://github.com/priyam0k/insurance-customer-segmentation.git)
    cd insurance-customer-segmentation
    ```

2.  **Install the dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the Jupyter Notebook:**
    ```bash
    jupyter notebook customer_segmentation_analysis.ipynb
    ```
    This will open the notebook in your browser, allowing you to execute the code cells and view the analysis step-by-step.

---

## 5. Business Impact

The personas identified in this analysis provide a clear roadmap for strategic business actions:

* **Personalized Marketing:** Develop tailored campaigns that speak to the specific needs of each segment (e.g., wellness programs for Cluster 1, family-focused plans for Cluster 2).
* **Improved Retention:** Design proactive retention strategies for the high-value, low-risk customers in Cluster 0.
* **Product Development:** Use insights from the segments to create new, relevant insurance products (e.g., affordable entry-level plans for Cluster 3).
* **Risk Management:** Better understand and price risk by recognizing the distinct characteristics of high-cost segments like Cluster 1.
