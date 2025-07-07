Dynamic Pricing for Urban Parking Lots
Summer Analytics 2025 – Capstone Project
Consulting & Analytics Club × Pathway

Overview
I developed this project as part of the Summer Analytics 2025 program. My goal was to build a dynamic pricing engine for urban parking lots using real-time data and economic logic. By adjusting prices based on demand, traffic, and special events, I aimed to optimize both parking utilization and revenue. I started with a simple linear pricing model and then implemented a more sophisticated demand-based approach.

Tech Stack
Python: For data analysis and modeling

Pandas, NumPy: For data manipulation and feature engineering

Matplotlib: For data visualization

Jupyter Notebook / Google Colab: For interactive development

GitHub: For version control and collaboration

Mermaid Live Editor: For creating the architecture diagram

Architecture Diagram
flowchart TD
    A[Raw Parking Data (CSV)] --> B[Data Preprocessing]
    B --> C[Feature Engineering]
    C --> D{Model Selection}
    D -->|Linear Model| E[Linear Pricing]
    D -->|Demand-Based Model| F[Demand-Based Pricing]
    E --> G[Visualization]
    F --> G
    G --> H[Interpretation & Reporting]
    H --> I[GitHub Submission]
    My Project Workflow
1. Data Ingestion
I loaded the provided dataset (dataset.csv) into a pandas DataFrame. I cleaned and preprocessed the data by handling missing values, stripping column names, and converting date/time columns.

2. Feature Engineering
I created features like occupancy ratio, demand score, and normalized demand. I also mapped categorical features (such as vehicle type and traffic condition) to numerical values for modeling.

3. Pricing Models
a. Baseline Linear Pricing
I started with a simple model where the price increases linearly with occupancy ratio:

linear_price = base_price + alpha * occupancy_ratio
b. Demand-Based Pricing
  Next, I built a model that considers occupancy, queue length, traffic, special days, and vehicle type:
  demand = (0.5 * occupancy_ratio) + (0.2 * queue_length) - (0.1 * traffic_level) + (0.1 * is_special_day) + vehicle_weight
  I normalized the demand and set the price as:
    demand_price = base_price * (1 + lambda * norm_demand)
  I kept the price within $5 and $20 to ensure realism.
  4. Visualization
I plotted the price evolution over time for sample parking lots, comparing both linear and demand-based pricing to show how responsive each model is.

5. Interpretation & Documentation
I summarized my findings, explained the model logic, and documented my assumptions. I also discussed limitations and possible improvements for the future.

6. Submission
I made sure all code runs without errors, added thorough explanations and comments, and prepared this well-structured README before making the repository public.

Repository Structure
.
├── README.md
├── data/
│   └── dataset.csv
├── notebooks/
│   └── dynamic_parking_pricing.ipynb
├── architecture/
│   └── architecture_diagram.md (or .png/.svg)

Key Findings
My demand-based pricing model is more responsive to real-world factors (like occupancy, events, and traffic) than the simple linear model.

The dynamic approach helps maximize both utilization and revenue by adjusting prices in real time.

The visualizations clearly show the advantages of demand-based pricing.

Assumptions & Limitations
I chose feature weights based on domain intuition and some trial and error.

I set price bounds ($5–$20) to prevent unrealistic pricing.

Traffic and vehicle types were mapped to numeric values for modeling.

I suggest adding competitive pricing and machine learning methods as future improvements.


