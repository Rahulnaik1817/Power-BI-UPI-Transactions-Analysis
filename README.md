# UPI Transactions Analysis Dashboard – Power BI

## 📊 Project Overview

This project is an interactive **UPI Transactions Analysis Dashboard** developed using **Microsoft Power BI**. The dashboard analyzes transaction volume, transaction value, success/failure rates, customer demographics, payment methods, banks, merchants, cities, transaction types, and other UPI transaction attributes.

The project is designed to demonstrate practical skills in **Data Analytics, Data Cleaning, Data Modeling, DAX, and Power BI Dashboard Development**.

## 🎯 Objectives

- Analyze overall UPI transaction performance.
- Track transaction count and transaction amount.
- Monitor successful and failed transactions.
- Identify transaction trends over time.
- Analyze transactions by city, bank, merchant, and transaction type.
- Understand customer demographics such as age and gender.
- Compare payment methods, devices, and payment modes.
- Identify important patterns and insights from UPI transaction data.
- Present the analysis through an interactive Power BI dashboard.

## 🗂️ Dataset

The project uses an Excel dataset containing **20,000 UPI transaction records**.

### Dataset Columns

| Column | Description |
|---|---|
| TransactionID | Unique transaction identifier |
| TransactionDate | Date of the transaction |
| Amount | Transaction amount |
| BankNameSent | Bank from which money was sent |
| BankNameReceived | Receiving bank |
| RemainingBalance | Customer balance after transaction |
| City | Customer transaction city |
| Gender | Customer gender |
| TransactionType | Type of transaction |
| Status | Transaction status |
| TransactionTime | Time of transaction |
| DeviceType | Device used for the transaction |
| PaymentMethod | Method used to make payment |
| MerchantName | Merchant involved in the transaction |
| Purpose | Purpose/category of the transaction |
| CustomerAge | Customer age |
| PaymentMode | Instant or scheduled payment |
| Currency | Transaction currency |
| CustomerAccountNumber | Customer account identifier |
| MerchantAccountNumber | Merchant account identifier |

> **Privacy Note:** The original dataset contains account-number fields. Avoid publishing real or sensitive financial information in a public repository. If the data is synthetic, clearly label it as synthetic; otherwise, remove/mask sensitive columns before publishing.

## 🛠️ Tools & Technologies

- **Microsoft Power BI Desktop**
- **Power Query** – Data cleaning and transformation
- **DAX** – Measures and calculated analysis
- **Microsoft Excel** – Source dataset
- **Git & GitHub** – Version control and project portfolio

## 📈 Key KPIs

The dashboard can be used to monitor KPIs such as:

- **Total Transactions**
- **Total Transaction Amount**
- **Average Transaction Amount**
- **Successful Transactions**
- **Failed Transactions**
- **Success Rate**
- **Failure Rate**
- **Average Remaining Balance**
- **Unique Merchants**
- **Unique Cities**
- **Transaction Count by Type**

## 📊 Dashboard Analysis

The dashboard provides analysis across multiple dimensions:

### Transaction Performance
- Total transaction volume
- Total transaction value
- Average transaction amount
- Success vs. failed transactions

### Time Analysis
- Transaction trends by date
- Monthly/periodic transaction patterns
- Transaction-time analysis

### Geographic Analysis
- Transactions by city
- Transaction amount by city
- City-level performance comparison

### Banking Analysis
- Sending bank analysis
- Receiving bank analysis
- Bank-to-bank transaction patterns

### Customer Analysis
- Gender distribution
- Customer age analysis
- Transaction behavior by demographic segments

### Payment Analysis
- Payment method distribution
- Payment mode comparison
- Device-type analysis
- Transaction-type analysis

### Merchant & Purpose Analysis
- Top merchants by transaction value
- Transaction purpose/category analysis
- Merchant transaction volume

## 🧮 Example DAX Measures

Example measures that can be created for this project:

```DAX
Total Transactions =
COUNTROWS('UPI Transactions')

Total Transaction Amount =
SUM('UPI Transactions'[Amount])

Average Transaction Amount =
AVERAGE('UPI Transactions'[Amount])

Successful Transactions =
CALCULATE(
    COUNTROWS('UPI Transactions'),
    'UPI Transactions'[Status] = "Success"
)

Failed Transactions =
CALCULATE(
    COUNTROWS('UPI Transactions'),
    'UPI Transactions'[Status] = "Failed"
)

Success Rate =
DIVIDE(
    [Successful Transactions],
    [Total Transactions],
    0
)
```

> Replace `'UPI Transactions'` with the actual table name in your Power BI model if it is different.

## 🔄 Data Preparation

The general workflow used in the project is:

1. Import the Excel dataset into Power BI.
2. Inspect data types and missing values.
3. Clean and transform data using Power Query.
4. Format date, time, numeric, and categorical fields.
5. Create calculated measures using DAX.
6. Build visualizations and KPI cards.
7. Add slicers and interactive filters.
8. Format the dashboard for clear business reporting.
9. Validate KPIs and dashboard results.

## 📁 Repository Structure

```text
UPI-Transactions-PowerBI/
│
├── UPI DATA.pbix
├── UPI+Transactions.xlsx
├── README.md
└── requirements.txt
```

## 🚀 How to Use

1. Clone or download this repository.
2. Install **Power BI Desktop**.
3. Open `UPI DATA.pbix`.
4. If Power BI asks for the source file, point the data source to `UPI+Transactions.xlsx`.
5. Refresh the data.
6. Explore the dashboard using slicers, filters, and visual interactions.

## 💡 Skills Demonstrated

- Data Cleaning
- Data Transformation
- Exploratory Data Analysis
- Power Query
- DAX
- Data Modeling
- KPI Development
- Dashboard Design
- Data Visualization
- Business Analysis
- Interactive Reporting
- GitHub Project Documentation

## 📌 Project Type

**Data Analytics | Business Intelligence | Power BI**

## 👨‍💻 Author

**Rahul Naik**

This project was created as part of my Data Analytics / Business Intelligence portfolio to demonstrate practical Power BI skills.

## ⭐ Future Improvements

- Add a dedicated date/calendar table.
- Add drill-through pages for bank and merchant analysis.
- Add advanced time-intelligence measures.
- Add anomaly/fraud-oriented transaction analysis.
- Publish the dashboard to Power BI Service.
- Add automated data refresh.
