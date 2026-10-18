# 📦 Supply Chain Data Modelling Streamlit App  

This Streamlit app is designed to provide **advanced analytics and data modelling** for **supply chain management in the pharmaceutical industry**.  

With this app, users can explore **forecasting, inventory optimisation, customer & product segmentation, and statistical analysis** to **enhance decision-making** in supply chain operations.  

---


## 🏗️ Project Structure

```bash
SupplyChainDataModellingStreamlit
├── .streamlit/
│   └── config.toml
├── assets/
│   └── data/
│       ├── DataGenerator.ipynb
│       └── pharmaceutical_supply_chain.csv
├── streamlit_app/
│   ├── pages/
│   │   ├── 01_1️⃣_Forecast_Demand.py
│   │   ├── 02_2️⃣_Inventory_Optimisation.py
│   │   ├── 03_3️⃣_Customer_Product_Segmentation.py
│   │   └── 04_4️⃣_Hypothesis_Testing.py
│   └── 00_ℹ️_Info.py
├── README.md
└── requirements.txt
```
---
## 🛠️ Features of the App  

The application consists of **four key modules**, each designed to address specific **supply chain challenges**:  

### **1️⃣ Forecast Future Demand (LSTM Model)**
- **What does it do?**  
  - Uses an **LSTM (Long Short-Term Memory) neural network** to forecast future demand based on historical sales data.  
  - Allows users to **select a specific SKU** and generate a **one-year demand forecast**.  
- **How does it work?**  
  - The **dataset is preprocessed** to remove non-stationarity and smooth variations in demand.  
  - A **train-test split (80%-20%)** ensures proper model validation.  
  - The **LSTM model** learns from historical sales data and predicts future trends.  
- **Output:**  
  - A **dynamic time-series forecast plot** showing **historical sales, predicted test values, and future forecasts**.  
  - **Mean Absolute Percentage Error (MAPE)** to measure model accuracy.  
  - A **downloadable table** of forecasted values for further analysis.  

### **2️⃣ Inventory Optimisation & Simulation**
- **What does it do?**  
  - Helps users optimise **inventory management** using:  
    - **Economic Order Quantity (EOQ)** – Determines the ideal order quantity to minimise costs.  
    - **Safety Stock Calculation** – Ensures **sufficient buffer stock** to prevent stockouts.  
    - **Monte Carlo Simulation** – Simulates **demand variations** using random sampling.  
- **How does it work?**  
  - Users can **select an SKU** and view **its optimal inventory parameters**.  
  - The **Monte Carlo simulation** generates **1000+ demand variations** to **predict uncertainty in sales**.  
- **Output:**  
  - **EOQ & Safety Stock values** displayed in a table.  
  - **Simulated demand distribution** to help estimate variability in sales.  
  - **Interactive visualisation** to analyse demand trends and supply chain risks.  

### **3️⃣ Customer & Product Segmentation**
- **What does it do?**  
  - Provides **segmentation insights** based on **sales performance and customer behaviour**.  
  - Users can explore:  
    - **Sales by Supplier** – Identify top-performing suppliers.  
    - **Sales by Product Family & Category** – Discover best-selling products.  
    - **Top & Bottom Customers** – Rank customers by **revenue contribution**.  
    - **Stock Turnover Analysis** – Understand inventory movement.  
- **How does it work?**  
  - Aggregates **sales, revenue, and stock turnover** across suppliers, categories, and products.  
  - Displays **interactive bar charts** to visualise performance metrics.  
- **Output:**  
  - **Top & Bottom 20 products** by **sales & stock turnover ratio**.  
  - **Supplier-wise sales trends** to assess **reliability & contribution**.  
  - **Customer segmentation based on revenue contribution**.  

### **4️⃣ Statistical Hypothesis Testing**
- **What does it do?**  
  - Conducts **five key statistical tests** to **validate supply chain insights**:  
    1. **Stockouts reduce sales** – Pearson correlation between stock level & sales.  
    2. **Longer lead times lower sales** – Linear regression between lead time & sales.  
    3. **Supplier revenue varies significantly** – Kruskal-Wallis test on supplier revenues.  
    4. **Frequent buyers generate more revenue** – Spearman correlation between purchase frequency & revenue.  
    5. **Certain categories generate higher revenue** – ANOVA test across product categories.  
- **How does it work?**  
  - Users can **select a hypothesis** from a dropdown menu.  
  - The app performs **statistical calculations** and plots the **test distribution, rejection region, and observed test statistic**.  
- **Output:**  
  - **Test results with p-value comparison to α = 0.05.**  
  - **Decision to reject or fail to reject the null hypothesis.**  
  - **Visual representation of the test statistic and rejection zone.**  

---

## 🎯 Why Use This App?
✔️ **Realistic Data Analysis:** Built using a **synthetic pharmaceutical supply chain dataset**.  
✔️ **End-to-End Workflow:** Covers **forecasting, inventory planning, customer segmentation, and validation tests**.  
✔️ **Business-Driven Insights:** Helps identify **demand trends, customer behaviour, and supplier performance**.  
✔️ **User-Friendly Interface:** Designed for **interactive data exploration and decision-making**.  

🚀 **Get started by selecting a module from the sidebar!**