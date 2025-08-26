# Advanced Customer Segmentation for Insurance Analytics

## 1. Project Overview

This project presents a comprehensive, end-to-end data science workflow for segmenting insurance policyholders using unsupervised machine learning. The core objective is to move beyond traditional, monolithic marketing and develop a nuanced, data-driven strategy. By identifying distinct customer personas, this analysis provides a framework to enhance customer engagement, reduce churn, and guide strategic business decisions in product development and risk management.

The analysis leverages a combination of **K-Means clustering**, **Hierarchical Clustering**, and **Principal Component Analysis (PCA)** to transform a raw dataset into actionable, high-value business intelligence.

---

## 2. Methodology

The analysis was conducted in a single Jupyter Notebook (`customer_segmentation_analysis.ipynb`) and follows a structured data science lifecycle.

* **Data Source:** An anonymized insurance dataset from a public GitHub repository.
* **Libraries:** Python, Pandas, Scikit-learn, Matplotlib, Seaborn, Plotly, SciPy.
* **Workflow:**
    1.  **Exploratory Data Analysis (EDA):** The dataset was inspected for quality and visualized using histograms, correlation matrices, and pair plots to uncover initial patterns and relationships.
    2.  **Feature Engineering:** New categorical features (`age_group`, `bmi_category`) were engineered from continuous variables to help the model identify clearer segment boundaries.
    3.  **Data Preprocessing:** All categorical features were one-hot encoded, and the resulting numerical dataset was standardized using `StandardScaler` to ensure all features contributed equally to the clustering models.
    4.  **Dimensionality Reduction:** PCA was applied to reduce the feature space to two principal components, enabling effective 2D visualization and reducing computational noise.
    5.  **Model Selection & Validation:** A dual-method approach was used to determine the optimal number of clusters (*k*):
        * **The Elbow Method** identified the point of diminishing returns for cluster compactness.
        * **Silhouette Score Analysis** quantitatively measured cluster separation, confirming the optimal *k*.
    6.  **Alternative Modeling:** Hierarchical Clustering with a dendrogram was used as a secondary method to validate the cluster structure.
    7.  **Profiling & Visualization:** The final cluster labels were mapped back to the original data to create detailed profiles. The segments were visualized using interactive scatter plots, comparative bar charts, and a holistic radar chart.

---

## 3. Key Findings: The Four Core Personas

The analysis successfully identified four distinct and commercially relevant customer personas:

* **Persona 0: Healthy & Low-Cost Non-Smokers:** A low-risk, high-value segment characterized by a healthy BMI, no smoking habits, and the lowest average insurance charges. This is a core group for retention strategies.
* **Persona 1: High-Risk, High-Cost Smokers:** This group is defined by high-cost claims, a high BMI, and a near-universal smoking habit. They represent a significant risk and cost factor for the business.
* **Persona 2: Mid-Risk Families:** This segment consists of older, non-smoking individuals with a higher BMI and more children. Their moderate insurance charges make them a stable and predictable customer base.
* **Persona 3: Young & Healthy Individuals:** The youngest segment with a low BMI and few dependents. Their low charges and long-term potential make them a prime target for acquisition and future cross-selling.

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
    This will open the notebook in your browser, allowing you to execute the code cells and view the complete analysis.

---

## 5. Business Impact

The personas developed in this project provide a clear roadmap for data-driven decision-making:

* **Personalized Marketing:** Craft campaigns that resonate with each persona's unique profile (e.g., wellness incentives for Persona 1, family-oriented benefits for Persona 2).
* **Strategic Retention:** Develop loyalty programs and proactive outreach for the high-value customers in Persona 0.
* **Customer Acquisition:** Target Persona 3 with affordable, entry-level products designed to capture long-term value.
* **Risk & Pricing Optimization:** Use the insights from high-risk segments like Persona 1 to inform more accurate underwriting and pricing models.
