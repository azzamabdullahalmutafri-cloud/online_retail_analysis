# Online Retail II Dataset Analysis 📊

A comprehensive exploratory data analysis (EDA) and business intelligence project analyzing e-commerce transaction data from the UCI Online Retail II dataset.

## 📋 Project Overview

This project provides an in-depth analysis of 525,461 e-commerce transactions across multiple dimensions:

- **Customer Segmentation**: RFM-based segmentation into 4 tiers (Occasional, Regular, Premium, VIP)
- **Product Performance**: Analysis of 4,070+ products by sales volume and revenue
- **Geographic Analysis**: Revenue distribution across 38 countries
- **Temporal Patterns**: Seasonal trends, monthly/weekly sales patterns
- **Customer Behavior**: Transaction frequency, spending patterns, product variety preferences

### Key Findings

- **Total Revenue**: £4.5M across analyzed transactions
- **Customer Base**: 4,140 unique customers
- **Geographic Dominance**: UK accounts for 65-70% of revenue
- **VIP Segment**: Top 10 customers generate 26% of total revenue
- **Seasonal Peak**: November-December holiday season drives 50%+ of annual revenue
- **Price-Demand**: Inverse relationship between product price and quantity sold

## 📂 Dataset Information

**Source**: [UCI Machine Learning Repository - Online Retail II](https://archive.ics.uci.edu/dataset/502/online+retail+ii)

**Dataset Details**:
- **Records**: 525,461 transactions
- **Time Period**: 2009-2011
- **Columns**: Invoice, StockCode, Description, Quantity, InvoiceDate, Price, Customer ID, Country
- **Data Type**: Transactional e-commerce data from a UK-based online retailer

## 🧹 Data Quality & Cleaning

### Issues Identified
- 3,690 records with zero or negative prices
- 9,288 records with missing customer IDs
- Outliers in quantity and price dimensions
- Potential duplicate/cancelled orders (invoices starting with 'C')

### Cleaning Process
1. Removed invalid records (non-positive prices)
2. Applied Interquartile Range (IQR) method for outlier detection
3. Removed 59,054 extreme outliers
4. Identified and handled cancelled transactions
5. **Final Dataset**: 466,471 clean, valid transactions

## 📊 Analysis Sections

### 1. **Data Quality Assessment** 
- Box plot analysis of price and quantity distributions
- Statistical summaries (mean, median, quartiles, std deviation)
- Data quality metrics before and after cleaning

### 2. **Business KPIs** 
- Total revenue, transaction count, unique customers
- Average order value, customer acquisition metrics

### 3. **Product Analysis** 
- Top 10 products by quantity and revenue
- Product category extraction and analysis
- Price distribution and price-demand relationships
- Slow-moving products identification
- Product performance statistics table

### 4. **Geographic Analysis** 
- Revenue by country (top 10)
- Market concentration analysis
- Export market insights

### 5. **Customer Analysis** 
- Top customers by spending and transaction frequency
- Customer segmentation (4 tiers):
  - **Occasional**: Low lifetime value, infrequent purchases
  - **Regular**: Moderate spending and frequency
  - **Premium**: High-value, consistent customers
  - **VIP**: Top spenders and most loyal customers
- Segment distribution and revenue contribution

### 6. **Customer Behavior Dashboards** 
- 4-chart integrated dashboard showing customer insights
- Spending distribution by segment
- Transaction frequency vs spending correlation
- Product variety by customer tier
- Detailed metrics and comparative statistics tables

### 7. **Temporal Analysis** 
- Monthly sales trends with seasonal patterns
- Day-of-week analysis
- Customer acquisition trends over time
- Best vs worst performing months
- Holiday season impact analysis

## 🛠️ Technologies & Libraries

- **Python 3.x**
- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computations
- **plotly.express**: Interactive data visualizations
- **Google Colab**: Cloud-based Jupyter environment

## 📈 Visualizations Included

The notebook contains **30+ interactive and static charts**:

✅ Box plots (price, quantity, spending distributions)  
✅ Bar charts (top products, customers, countries)  
✅ Pie charts (customer segment distribution)  
✅ Scatter plots (price vs quantity, frequency vs spending)  
✅ Line charts (temporal trends, monthly sales)  
✅ Histograms (price distribution)  
✅ Heatmaps & dashboards (integrated business intelligence views)  
✅ Summary tables (detailed metrics)

## 🚀 Quick Start

### Prerequisites
```bash
pip install -r requirements.txt
```

### Running the Notebook

1. **Google Colab** (Recommended):
   - Open the notebook in Google Colab
   - Mount your Google Drive if needed
   - Run all cells in sequence

2. **Local Jupyter**:
   ```bash
   jupyter notebook online_retail_analysis.ipynb
   ```

### Notes
- The notebook was developed in Google Colab; adjust file paths if running locally
- First code cell handles Drive mounting; can be skipped for local execution
- All visualizations are interactive (Plotly)
- Estimated runtime: 2-5 minutes depending on hardware

## 💡 Key Insights & Use Cases

### For E-commerce Teams
- **Customer Strategy**: Focus retention efforts on VIP segment (26% of revenue from 10 customers)
- **Inventory Planning**: Prioritize products in top 50 by revenue; consider discontinuing slow-movers
- **Geographic Expansion**: UK market mature; high growth potential in growing markets
- **Seasonal Planning**: Allocate marketing budget for Nov-Dec holiday peak

### For Data Scientists
- **Segmentation Model**: Use RFM scores as base for ML-based customer clustering
- **Churn Prediction**: Track VIP customer transaction patterns for early warning
- **Price Optimization**: Analyze price elasticity; opportunity for premium product positioning
- **Forecasting**: Seasonal ARIMA/Prophet models for monthly revenue prediction

### For Business Analysts
- **KPI Dashboard**: Template for monitoring key metrics
- **Customer Tiers**: Framework for loyalty program design
- **Product Portfolio**: Data-driven product lifecycle management
- **Market Analysis**: Geographic expansion opportunities

## 📊 Analysis Depth

This is an **intermediate-to-advanced EDA** project featuring:

- ✅ Multi-dimensional analysis (customer, product, geographic, temporal)
- ✅ Data quality assessment and sophisticated cleaning techniques
- ✅ RFM customer segmentation with statistical validation
- ✅ Correlation analysis and pattern discovery
- ✅ Interactive visualizations with Plotly
- ✅ Business metric calculation and KPI tracking
- ✅ Comparative analysis across segments
- ✅ Actionable insights and recommendations

## 🔄 Reproducibility

- All analysis is deterministic (no random sampling)
- Data source is public and permanently available
- Complete code is documented with markdown explanations
- Steps are sequential and can be re-run independently
- No external API keys or authentication required (except Google Drive mounting for Colab)

## 📚 Data Dictionary

| Column | Description | Type |
|--------|-------------|------|
| Invoice | Unique transaction ID | String |
| StockCode | Product identifier | String |
| Description | Product name/description | String |
| Quantity | Units purchased | Integer |
| InvoiceDate | Transaction date/time | DateTime |
| Price | Unit price (£ GBP) | Float |
| Customer ID | Unique customer identifier | Integer |
| Country | Purchase country | String |

## 🤝 Contributing

This project is provided as-is for educational and analytical purposes. Feel free to:
- Fork and extend the analysis
- Apply techniques to other datasets
- Create alternative visualizations
- Develop predictive models based on this EDA

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

The Online Retail II dataset is publicly available from the UCI Machine Learning Repository and is used for educational and non-commercial purposes in accordance with the repository's terms.

## 📞 Citation

If you use this analysis in your work, please cite:

```
Online Retail Analysis Project
Based on: Online Retail II Dataset
Source: UCI Machine Learning Repository
URL: https://archive.ics.uci.edu/dataset/502/online+retail+ii
```

---

**Created**: 2024  
**Version**: 1.0  
**Status**: Complete EDA ready for production analysis and model development
