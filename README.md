# freelance-sales-analysis
 Analysis and presentation of data-driven insights for real-world application in an e-commerce user store following Google's six stage analysis process: Ask, Prepare, Process, Analyze, Share, Act.
 
## Ask

How can the client optimize their inventory and avoid products stagnating in storage?

Which regions and customer segments are exhibiting the most growth in sales over time?

What data-driven actions should the client pursue in order to optimize operations, given the results of the questions above?

## Prepare

Annual sales datasets were downloaded from the user's Mercari store profile. I imported the CSV files to a Python kernel in VSCode, where I used Pandas operations to concatenate the three datasets into one. There are 1,732 unique observations of sales, and 17 attributes including product name, sale date, sale price, net proceeds, shipping cost, and customer state of residence. 

## Process

First, I deleted irrelevant columns that did not provide information, for example: I deleted the attribute "Shipped From State", because it was the same for every observation. I used Pandas and Numpy operations such as np.unique(), pd.value_counts(), and pd.isna() in order to detect errors and NaNs in the dataset. I found multiple erroneous rows with missing or incomplete data. After applying systematic cleaning, I exported the file to a Google Sheet, where I took a closer, more hands-on look at the dataset. Here, I found additional errors such as extra whitespaces and improper data separation, and manually corrected them. 

## Analyze

After data preprocessing, I connected the dataset to Tableau, where I created new calculated fields with aggregates, averages, and coutns of sales attributes such as buyer location, item price, quantity of sales, and annual sales growth. I compared these attributes across geographical locations by drafting figures in Tableau. These quick figures were able to show trends in the data, and progressed my analysis to more specific answers.

I started by performing initial EDA to see which states are selling the most items, and the average price of each item based on state.

Item Sold Price by State

![avg_item_price_by_state](https://user-images.githubusercontent.com/58805376/177470027-84a335ed-1f0a-432e-b46c-b0d011c8c8db.png)

Number of Items Sold by State

![Screenshot_72](https://user-images.githubusercontent.com/58805376/177470562-aab92861-51d5-46af-a2fb-3f7345f8ca33.png)

Then, I broke the sales down into the proportion of total order quantity per state (computed in Python), over the course of three years. This way, we can analyze trends in geographic sales data and see which states are having growth or decline in orders.

![2020sales](https://user-images.githubusercontent.com/58805376/177620066-dd8880e8-a26c-48d2-9b89-775844e3196f.png)

![2021sales](https://user-images.githubusercontent.com/58805376/177620108-600f2682-b837-4428-a465-0997d1a6f9de.png)

![2022sales](https://user-images.githubusercontent.com/58805376/177620117-a342e1a8-1c1e-4e8f-8e29-2b34cd104cee.png)

This visualization allows me to see that sales in NY are declining over time, and that the Southeast and Midwest regions of the United States are seeing the most growth in sales. Namely, Ohio, Texas, and Missouri are major contributors to the overall sales landscape. Thus, the client should tailor their inventory to meet the purchasing habits of these segments.

## Share

I compiled my visualizations into a report that was comprehensible for the non-technical client and communicated my data-driven findings. The client reported that my report led to a more sophisticated understanding of their customer base and the factors that lead to sales. 

## Act

After presentation, I suggested that the client make calculated decisions when choosing their inventory and listings. An example includes stocking up on inventory that is in high demand among growing customer segments given past trends, while avoiding inventory that has downward trending demand.


