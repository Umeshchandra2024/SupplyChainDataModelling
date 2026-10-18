# 💊 Pharma Supply Chain Analytics Studio

An interactive **Streamlit** app for **data-driven decision making in pharmaceutical supply chains**.

It brings together **demand forecasting, inventory control, segmentation insights, and statistical validation** in one place, so planners and analysts can move from raw data to confident decisions quickly.

---

## 🗂️ Project Structure

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

## ⚙️ App Modules

The app is organised into **four modules**, each targeting a common supply chain problem.

### 📈 1. Demand Forecasting (LSTM)

**Purpose**
- Predicts future demand for a chosen SKU using an **LSTM (Long Short-Term Memory)** neural network trained on past sales.
- Produces a **12-month forward forecast** for any selected product.

**Approach**
- The data is cleaned and transformed to **remove non-stationarity** and smooth out noise.
- An **80/20 train-test split** is used to validate the model before forecasting.
- The trained network learns historical patterns and projects them forward.

**What you get**
- An **interactive time-series chart** combining actual sales, test predictions, and the future forecast.
- **MAPE (Mean Absolute Percentage Error)** as a measure of forecast accuracy.
- A **downloadable forecast table** for use in other tools.

### 🏭 2. Inventory Optimisation & Simulation

**Purpose**
- Helps determine how much to order and how much buffer to hold, using:
  - **EOQ (Economic Order Quantity)** – the order size that minimises total cost.
  - **Safety Stock** – a buffer that protects against stockouts.
  - **Monte Carlo Simulation** – random sampling to model demand uncertainty.

**Approach**
- Pick an SKU to see its **recommended inventory parameters**.
- The simulation runs **1,000+ demand scenarios** to show how much sales can vary.

**What you get**
- A summary table of **EOQ and safety stock** values.
- A **distribution of simulated demand** that reveals variability and risk.
- **Interactive charts** for exploring trends and supply risks.

### 🧩 3. Customer & Product Segmentation

**Purpose**
- Breaks down performance by **supplier, product, and customer** to show where value comes from.
- Lets you explore:
  - **Supplier Sales** – spot your strongest partners.
  - **Product Family & Category Sales** – find the best sellers.
  - **Top & Bottom Customers** – rank accounts by revenue share.
  - **Stock Turnover** – see how quickly inventory moves.

**Approach**
- Sales, revenue, and turnover are **aggregated** across suppliers, categories, and products.
- Results are shown as **interactive bar charts**.

**What you get**
- **Top and bottom 20 products** by sales and turnover ratio.
- **Supplier trend views** to judge reliability and contribution.
- **Customer groupings** based on revenue contribution.

### 🧪 4. Statistical Hypothesis Testing

**Purpose**
- Runs **five statistical tests** to check whether common supply chain assumptions hold up:
  1. **Stockouts hurt sales** – Pearson correlation between stock level and sales.
  2. **Longer lead times reduce sales** – linear regression of lead time against sales.
  3. **Supplier revenues differ** – Kruskal-Wallis test across suppliers.
  4. **Frequent buyers bring in more revenue** – Spearman correlation of purchase frequency and revenue.
  5. **Revenue differs by category** – ANOVA across product categories.

**Approach**
- Choose a hypothesis from the dropdown.
- The app calculates the test and plots the **distribution, rejection region, and observed statistic**.

**What you get**
- **p-value compared against α = 0.05**.
- A clear **reject / fail to reject** decision for the null hypothesis.
- A **visual** showing where the result falls relative to the rejection zone.

---

## 🌟 Why This App?

- 🧬 **Realistic data:** built on a **synthetic pharmaceutical supply chain dataset**.
- 🔁 **Complete workflow:** from forecasting and inventory planning to segmentation and statistical validation.
- 💡 **Actionable insights:** surfaces demand patterns, customer behaviour, and supplier performance.
- 🖱️ **Easy to use:** interactive controls make exploration simple, even for non-programmers.

🚀 **Ready to begin? Pick a module from the sidebar.**
