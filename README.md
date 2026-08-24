# UPI Transactions Dashboard — Power BI

An interactive Power BI dashboard that analyzes 20,000+ UPI (Unified Payments Interface) transactions across Indian cities for the year 2024. The report tracks transaction volume, amounts, and running account balance over time, with rich slicing across banks, cities, devices, demographics, and payment attributes.

## 📊 Overview

This project explores UPI transaction data to surface trends in monthly transaction activity and balance movement, and to enable deep-dive filtering by bank, city, merchant, payment mode, and customer demographics. Users can toggle between column and line chart views for both **Amount** and **Balance**, and drill into a city/currency matrix for granular monthly figures.

## 🗂️ Files in this Repository

| File | Description |
|---|---|
| `UPI_DATA.pbix` | The Power BI report file (open with Power BI Desktop) |
| `UPI_Transactions.xlsx` | Source dataset (20,000+ transaction records) |
| `screenshots/` | Dashboard preview images |

## 📁 Dataset

The dataset (`UPI_Transactions.xlsx`) contains ~20,000 transaction records with the following fields:

- **Transaction details:** `TransactionID`, `TransactionDate`, `TransactionTime`, `Amount`, `RemainingBalance`, `Status`, `TransactionType`
- **Parties:** `BankNameSent`, `BankNameReceived`, `MerchantName`, `CustomerAccountNumber`, `MerchantAccountNumber`
- **Demographics:** `Gender`, `CustomerAge`, `City`
- **Payment attributes:** `DeviceType`, `PaymentMethod`, `PaymentMode`, `Purpose`, `Currency`

## 🖥️ Dashboard Features

- **Global slicers:** BankNameSent, BankNameReceived, City, DeviceType, Gender, Age Group, MerchantName, PaymentMode, Purpose, TransactionType
- **Toggle views:** switch each chart between Column and Line, for both Transaction Amount and Balance
- **Monthly trend analysis:** transaction amount and balance patterns across all 12 months of 2024
- **City/Currency matrix:** monthly Amount and Remaining Balance broken out by City and Currency (Bangalore/EUR, Delhi/USD, Hyderabad/GBP, Mumbai/INR, etc.)

## 📸 Dashboard Previews

### Transactions by Month — Column Chart
<img width="1273" height="718" alt="Image" src="https://github.com/user-attachments/assets/3946c988-aeae-4471-a218-e9fed3fc40a7" />

### Transactions by Month — Line Chart
<img width="1271" height="708" alt="Image" src="https://github.com/user-attachments/assets/27bad0b5-0dbb-4750-825f-bfcc931cdead" />

### Balance by Month — Column Chart
<img width="1274" height="712" alt="Image" src="https://github.com/user-attachments/assets/6bb7f4b4-09ce-4466-9b91-6bb38e89d311" />

### Balance by Month — Line Chart
<img width="1274" height="715" alt="Image" src="https://github.com/user-attachments/assets/1a9ee20c-0327-4edf-a7af-9eb938a4ca30" />

### City / Currency Matrix View
<img width="1268" height="714" alt="Image" src="https://github.com/user-attachments/assets/6883218e-e8c9-46b2-9c21-0db0caa7085e" />

## 🚀 Getting Started

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Windows only).
2. Clone or download this repository.
3. Open `UPI_DATA.pbix` in Power BI Desktop.
4. If prompted, point the data source to `UPI_Transactions.xlsx` in this repo.
5. Use the slicers and chart-toggle buttons at the top of each page to explore the data.

## 🛠️ Tools Used

- **Power BI Desktop** — data modeling, DAX measures, and report design
- **Excel** — source data storage

## 📌 Notes

- Report year in view: **2024**
- Currency values vary by city (INR, USD, EUR, GBP) as reflected in the matrix visual.

## 📄 License

This project is shared for portfolio and educational purposes. Feel free to fork and adapt.
