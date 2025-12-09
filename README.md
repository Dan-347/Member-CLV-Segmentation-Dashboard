# Member CLV Segmentation Dashboard

![XYZ_Member_Dashboard](https://github.com/user-attachments/assets/7ec885fa-a014-4682-a7f6-13a1fe0d4ce9)

This dashboard was developed as the final result of Customer Lifetime Value (CLV) analysis and customer segmentation using a combination of probabilistic models (BG/NBD & Gamma-Gamma) and unsupervised learning (K-Means based on LRFM + CLV). This dashboard aims to help the Marketing and Data teams at Retail XYZ understand customer characteristics from two main perspectives, namely historical behavior (LRFM) and future economic value potential (CLV value).

Through this dashboard, users can visually view customer segmentation, understand the differences between each segment, and identify customer groups that have strategic value for the business.

## Background
In the business world, customers are an important aspect that determines the sustainability of a company's business. Not only as a source of income, customers also play a major role in contributing to and reflecting the value brought to the company's development, whether through activities, interactions, feedback, or loyalty. Every activity carried out by customers provides deep insights into their behavior and purchasing preferences. Understanding these insights gives companies the ability to optimize their marketing strategies, increase customer loyalty, and develop and offer products or services that meet customer needs. Data such as customer activities or transactions contain important information that can be the most valuable asset for companies in understanding these insights to support operational success and decision-making processes. Information from customer activity data also helps companies identify patterns or trends that may emerge from customer interactions with the business.

Based on the results of surveys and interviews at XYZ retail,  currently, the marketing team in particular is having difficulty understanding customer quality and behavior, as well as identifying high-value customers. The team also finds it difficult to know which customers to retain or target in a marketing campaign, so marketing strategies are often general and less targeted, risking inefficient promotion budget allocation, decreased customer retention, and loss of potential revenue from high-value customers. In addition, the company does not yet have a visualization tool that can help monitor and evaluate changes in customer behavior and value. Therefore, the marketing team needs a solution that can help them analyze customer data more effectively and efficiently.

## Objectives
This project was developed with the aim to:
1. Integrating analytical methods with dashboards to present complex information in a simpler and more understandable way for non-technical users.
2. Identify and predict customer value, both in terms of revenue and future growth potential.
3. Segmenting customers based on similar behavior patterns and values, forming customer groups with unique characteristics.
4. Designing interactive visualizations that present customer CLV information.

## Why This Analysis Matters
The benefits that can be provided in this project are as follows:
1. Providing insight into the characteristics of each customer segment and its contribution to the company.
2. Assist the marketing team in identifying potential customers to determine effective and efficient marketing strategies to improve customer satisfaction.
3. Improve customer retention and reduce churn risk, while encouraging customer loyalty.
4. Assisting companies in predicting revenue and measuring the future Return on Investment (ROI) they will receive.
5. Optimizing resource allocation based on an understanding of customer behavior, so that business strategies are more targeted.
6. Supporting more accurate decision-making through a data-driven approach by providing comprehensive insights into customer behavior and values.

This dashboard is highly relevant for:
1. Marketing Team → creating promotion and retention strategies
2. CRM/Customer Success → determining differentiated treatment for each segment
3. Data Team → monitoring customer behavior
4. Management → viewing a macro overview of customer value

## Analysis Steps
There are six stages in this project, with an explanation of each step as follows:
1. **Data Collection** <br>
This study uses XYZ retail data mart, particularly transaction and customer data. Transaction data contains records of customer purchases from January 1, 2023, to June 30, 2024. Customer data is used in the dashboard visualization stage to display customer information, while transaction data is used in the probability and clustering analysis stage to understand customer purchasing behavior patterns.
2. **Data Cleaning** <br>
Before conducting the analysis stage, transaction data needs to be cleaned to ensure the quality of the data used in the analysis. At this stage, irrelevant transaction data, such as canceled transactions, will be deleted, data formats such as dates and numerical values will be checked and adjusted, and missing values will be handled.
3. **Application of the BG/NBD Model** <br>
The cleaned data will be used to predict future customer behavior. The BG/NBD Model focuses on the variables of frequency, recency, and T to determine repeat customer transaction behavior. The process of implementing this model includes dividing the data into training and test data, training the model, evaluating or testing the model, applying it to all data, and predicting the number of transactions and lifetime probability for each customer.
4. **Application of the Gamma-Gamma Model** <br>
Next, applying the gamma-gamma model to predict the CLV value of each customer. The gamma-gamma model focuses on monetary and frequency variables to determine the estimated average amount of money spent by customers in transactions and is used to calculate the predicted CLV value. This model also has several processes that must be followed, such as training the model, evaluating the model, and predicting the CLV value
5. **Application of K-Means Clustering** <br>
The next step is to group customers based on the prediction results. The data will be divided into several groups or clusters based on the similarity between data in one group. The K-Means algorithm can be used in CLV to group customers based on behavior patterns and profit value. The clustering process involves several steps, such as LRFM extraction, data normalization, finding the optimal number of clusters using the Elbow Method and Silhouette Score, and performing clustering using the best number of clusters. The clustering results will then be analyzed in more depth regarding the characteristics of each segment.
6. **Dashboard Design** <br>
The results of the probability analysis and segmentation that have been tested will be visualized in the form of a dashboard. The dashboard design is necessary to facilitate the reading and understanding of the data analysis results. With the dashboard, data that was originally in the form of text and numbers will be converted into graphs so that stakeholders can easily see patterns or trends and make the right decisions based on the data.

## Insights
1. **BG/NBD Model and Gamma-gamma Model**
Based on the results of BG/NBD model training on training data, the parameters indicate that most customers have a low purchase frequency, while only a small portion transact intensively and are highly active. This condition results in a fairly wide distribution of purchase levels. In addition, parameter estimates also indicate that the probability of customers becoming inactive is relatively high, in line with the general pattern of retail customers who make a limited number of transactions. The model evaluation was conducted visually and quantitatively; both approaches showed low error rates and were still within reasonable limits, thus reinforcing that the model has sufficient precision in predicting overall purchasing behavior. The BG/NBD model was then retrained using all transaction data to obtain more stable and representative estimation parameters. This model was then used to calculate estimates of future customer transactions and the probability of customers remaining active.

After modeling customer purchase frequency using BG/NBD, the next step is to predict the average transaction value of customers using the Gamma-Gamma Model. In accordance with the basic assumptions of this model, only customers who have made more than one transaction can be analyzed. Based on the training results, the Gamma-Gamma parameters indicate that there is considerable variation in average spending between customers. This indicates that some customers consistently have higher transaction values than others. Parameter estimates also show that the overall average spending pattern per transaction is in line with the distribution of spending among customers, although there is still significant variation between them. In other words, despite striking differences between customers, the spending behavior of each individual tends to be stable over time. The evaluation of the model in predicting the average transaction value shows that the relative percentage error is low, while the absolute error is still acceptable considering that customer transaction values vary and can reach high nominal values. Overall, these results show that the Gamma-Gamma Model is capable of producing fairly accurate and reliable average spending estimates as a component of CLV calculations.

2. **K-Means Clustering**


3. **Dashboard**

## Conclusion
