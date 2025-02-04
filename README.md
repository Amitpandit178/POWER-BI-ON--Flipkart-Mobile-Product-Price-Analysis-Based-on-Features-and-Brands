# 🚀 Flipkart Mobile Product Price Analysis Based on Features and Brands 🚀

## 📌 Project Overview

The *Flipkart Mobile Product Price Analysis* project focuses on analyzing smartphone pricing trends on Flipkart, considering various *features, brands, and specifications. The goal is to provide data-driven insights to help consumers, businesses, and analysts understand price distributions, key features influencing cost, and brand-wise performance. The project leverages **Power BI* to create an *interactive dashboard* for visualizing patterns and trends in mobile phone pricing.

## 🛠 Tools & Technologies Used

- *Power BI*: Data visualization and interactive dashboard creation.
- *DAX (Data Analysis Expressions)*: Used for complex calculations and performance metrics.
- *Excel/CSV Data Processing*: Cleaning and transforming datasets.
- *Mapping Tools*: Integrated visualizations for better insights into brand distribution.

## 📊 Data Insights & Key Findings

### *1️⃣ Price Categorization of Mobile Phones*
The dataset categorizes phones into three price segments:
- *Budget Phones* (₹5,000 – ₹15,000)
- *Mid-Range Phones* (₹15,000 – ₹30,000)
- *Premium Phones* (₹30,000+)

The analysis found:
- *392 models* fall into the Mid-Range segment (most popular category).
- *260 models* are categorized as Premium phones.
- *123 models* belong to the Budget category.

### *2️⃣ Brand-wise Price Analysis*
- *Google* has the highest average selling price (*₹67K*).
- *Samsung, Xiaomi, and Realme* dominate the Mid-Range category.
- *Apple and Google* lead the Premium segment with high-end devices.
- *Infinix, Tecno, and Micromax* focus on Budget-friendly smartphones.

### *3️⃣ Feature-Based Pricing Analysis*
- *RAM & Storage Impact on Price*:
  - Phones with *8GB+ RAM* and *256GB+ storage* generally fall in the Premium category.
  - *4GB RAM models* dominate the Budget segment.
  
- *Camera Analysis*:
  - Higher *back-camera MP (108MP and above)* significantly increases price.
  - *Front-camera MP (16MP and above)* correlates with better customer ratings.

- *5G vs Non-5G Pricing Trends*:
  - *5G phones* have a higher average selling price (~₹26,471) than *non-5G* (~₹24,241).
  - *563 high-rated 5G phones* were identified compared to *204 non-5G* models.

### *4️⃣ Market Demand & Consumer Preferences*
- *Total Models Available: **775*
- *Average Selling Price: **₹26,000*
- *Maximum Price: **₹1,62,000*
- *Minimum Price: **₹5,499*
- *Total Sales: **20M+ units*

### *5️⃣ Correlation Between Price & Ratings*
- Phones in the *₹5,000 – ₹15,000* price range receive the highest number of customer ratings.
- Devices priced *above ₹50,000* have fewer ratings but maintain higher brand loyalty.
- The *price-rating correlation* is *-0.16, meaning **higher-priced models do not always receive the best ratings*.

---

## ⚙ DAX Formulas Used

### *1️⃣ Total Sales Calculation*
DAX
Total Sales = SUM(SalesData[Sales])

Calculates the total number of mobile units sold.

### *2️⃣ Average Selling Price*
DAX
Avg Selling Price = AVERAGE(SalesData[Selling Price])

Finds the average price across all mobile brands.

### *3️⃣ Maximum and Minimum Price*
DAX
Max Price = MAX(SalesData[Selling Price])
Min Price = MIN(SalesData[Selling Price])

Determines the highest and lowest prices in the dataset.

### *4️⃣ Price Segmentation (Budget, Mid-Range, Premium)*
DAX
Price Category =
SWITCH(
    TRUE(),
    SalesData[Selling Price] <= 15000, "Budget",
    SalesData[Selling Price] > 15000 && SalesData[Selling Price] <= 30000, "Mid-Range",
    SalesData[Selling Price] > 30000, "Premium"
)

Categorizes phones based on their price range.

### *5️⃣ 5G vs Non-5G Price Difference*
DAX
5G Price Difference =
CALCULATE(AVERAGE(SalesData[Selling Price]), SalesData[Is_5G] = TRUE()) -
CALCULATE(AVERAGE(SalesData[Selling Price]), SalesData[Is_5G] = FALSE())

Finds the difference in average selling prices between *5G and Non-5G models*.

### *6️⃣ Count of Models per Brand*
DAX
Models Per Brand = COUNT(SalesData[Model Name])

Counts the total number of models available per brand.

### *7️⃣ Average Rating by Price Category*
DAX
Avg Rating by Category =
CALCULATE(
    AVERAGE(SalesData[Customer Rating]),
    ALLEXCEPT(SalesData, SalesData[Price Category])
)

Computes the average customer rating for each *price category* (Budget, Mid-Range, Premium).

### *8️⃣ Correlation Between Price and Ratings*
DAX
Correlation_Price_Rating =
CORREL(SalesData[Selling Price], SalesData[Customer Rating])

Finds the statistical correlation between *price and customer ratings*.

---

## 🔍 How to Use the Power BI Dashboard

1. *Open the Power BI File*:
   - Install *Power BI Desktop* (if not installed).
   - Open the Flipkart_Mobile_Analysis.pbix file.

2. *Explore Pricing Trends*:
   - Use *filters* for brand-wise, feature-based, and category-based price analysis.
   - Compare the *impact of 5G vs non-5G* on selling price.

3. *Analyze Feature Popularity*:
   - View trends on *RAM, battery, and camera specs* affecting price.
   - Check which brands dominate in the Budget, Mid-Range, and Premium categories.

4. *Generate Reports & Share Insights*:
   - Export *customized reports* in Power BI.
   - Share insights with stakeholders for better decision-making.

---

## 🚀 Future Enhancements

- *Real-time Data Integration*: Automating updates from Flipkart listings.
- *Sentiment Analysis*: Extracting insights from customer reviews and ratings.
- *Predictive Pricing Model: Using **machine learning* to forecast price trends.
- *Comparative Brand Performance*: Comparing Flipkart pricing with Amazon or other e-commerce platforms.

---

## 📩*For queries, contributions, or collaborations, feel free to reach out:*
- Amit Pandit
- Amarendra Nayak and Jagyansu Padhy
- Contact 📧: amitpandit175@gmail.com, toamarendranayak@gmail.com and jagyansup@gmail.com

---

This README provides an in-depth *technical and business overview* of the project, along with *all the DAX formulas used* in Power BI. 🚀
```
🚀 Let me know if you need any modifications!
