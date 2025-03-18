# MARKET BASKET ANALYSIS USING ECLAT ALGORITHM
This project focuses on analyzing customer purchasing behavior by applying ECLAT algorithm to discover frequent itemsets and strong association rules. The dataset used is Google Retail, containing over 165,000 transactions and 1,178 unique products. The analysis provides actionable insights for businesses to optimize product bundling and enhance sales strategies.

# Research Objectives:
  - Identify frequent itemsets in retail transactions to understand product associations.
  - Extract strong association rules to support business decision-making (e.g., product bundling, promotions).
  - Compare ECLAT with Apriori and FP-Growth algorithms to evaluate efficiency.
# Key Features:
  - Preprocessed data (cleaning, handling missing values, transforming format).
  - Performed Exploratory Data Analysis (EDA) to identify top-selling products and seasonal trends.
  - Implemented ECLAT in Python, extracting frequent itemsets and strong association rules.
  - Compared ECLAT, Apriori, and FP-Growth algorithms, demonstrating ECLAT’s efficiency in mining frequent patterns.
  - Provided business insights for improving product recommendations and promotional strategies.
# EDA 
![image](https://github.com/user-attachments/assets/cff2c5ca-6e56-4ea7-b840-2438b1b01f30)
  - The chart displays the top 10 most frequently appearing StockCodes. StockCode 20725 leads with nearly 1600 appearances, indicating high demand. Following closely are 22197, 21212, and 20727, each appearing between 1200 and 1400 time. The remaining StockCodes in the top 10 have appearances ranging from 1000 to 1200, showing consistent demand. Notably, all items in this list appear more than 1000 times, emphasizing their importance. These insights can help optimize inventory management, pricing strategies, and promotional efforts to enhance business performance.
![image](https://github.com/user-attachments/assets/c57b5878-db81-4022-b3a9-2684d6ac5f34)
  - The chart illustrates the top 10 invoices with the highest number of StockCodes. Invoice 573585 stands out with the most StockCodes, exceeding 350, significantly higher than the rest. The second-highest, 558475, contains just over 300, followed closely by others ranging from 250 to 300 StockCodes. The relatively small gap between invoices ranked 3rd to 10th suggests a fairly even distribution among them. This insight highlights key invoices with large product variations, which could be useful for analyzing bulk purchases or identifying high-value transactions.
![image](https://github.com/user-attachments/assets/883f123b-b94d-4f0d-b7ac-c5b081f5c800)
![image](https://github.com/user-attachments/assets/4411ef5a-f4d3-449c-ad4d-b1c9582472b6)
    **StockCode Quantity Over Time Chart**
  - January and December 2017 had the highest number of StockCodes, with December reaching the peak. This may be due to strong year-end promotions such as Christmas, New Year, and Black Friday, when shopping demand increases.
On the other hand, months like March and June had lower sales, possibly because they are not peak shopping seasons.

    **Number of Orders per Month Chart**
  - December also had the highest number of orders, indicating more customers were purchasing.
January had a high StockCode quantity but a lower number of orders, which could mean fewer customers were buying, but they purchased in larger quantities (possibly businesses or wholesale buyers). November ranked second in order volume, aligning with major sales events like Black Friday and Cyber Monday, when customer demand increases.

# ECLAT Agorithim

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>antecedents</th>
      <th>consequents</th>
      <th>support</th>
      <th>confidence</th>
      <th>lift</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>(21086)</td>
      <td>(21094)</td>
      <td>0.021002</td>
      <td>0.818396</td>
      <td>25.953057</td>
    </tr>
    <tr>
      <th>1</th>
      <td>(21094)</td>
      <td>(21086)</td>
      <td>0.021002</td>
      <td>0.666027</td>
      <td>25.953057</td>
    </tr>
    <tr>
      <th>2</th>
      <td>(21094)</td>
      <td>(21080)</td>
      <td>0.022213</td>
      <td>0.704415</td>
      <td>12.047969</td>
    </tr>
    <tr>
      <th>3</th>
      <td>(20723)</td>
      <td>(20719)</td>
      <td>0.023786</td>
      <td>0.560628</td>
      <td>11.435420</td>
    </tr>
    <tr>
      <th>4</th>
      <td>(20719)</td>
      <td>(20723)</td>
      <td>0.023786</td>
      <td>0.485185</td>
      <td>11.435420</td>
    </tr>
    <tr>
      <th>5</th>
      <td>(20724)</td>
      <td>(20723)</td>
      <td>0.028507</td>
      <td>0.469124</td>
      <td>11.056860</td>
    </tr>
    <tr>
      <th>6</th>
      <td>(20723)</td>
      <td>(20724)</td>
      <td>0.028507</td>
      <td>0.671897</td>
      <td>11.056860</td>
    </tr>
    <tr>
      <th>7</th>
      <td>(20719)</td>
      <td>(20724)</td>
      <td>0.029657</td>
      <td>0.604938</td>
      <td>9.954970</td>
    </tr>
    <tr>
      <th>8</th>
      <td>(20724)</td>
      <td>(20719)</td>
      <td>0.029657</td>
      <td>0.488048</td>
      <td>9.954970</td>
    </tr>
    <tr>
      <th>9</th>
      <td>(21929)</td>
      <td>(21928)</td>
      <td>0.023605</td>
      <td>0.463183</td>
      <td>9.723898</td>
    </tr>
    <tr>
      <th>10</th>
      <td>(21928)</td>
      <td>(21929)</td>
      <td>0.023605</td>
      <td>0.495553</td>
      <td>9.723898</td>
    </tr>
    <tr>
      <th>11</th>
      <td>(20712)</td>
      <td>(21931)</td>
      <td>0.026450</td>
      <td>0.521480</td>
      <td>7.498597</td>
    </tr>
    <tr>
      <th>12</th>
      <td>(21930)</td>
      <td>(21931)</td>
      <td>0.021244</td>
      <td>0.516937</td>
      <td>7.433270</td>
    </tr>
    <tr>
      <th>13</th>
      <td>(21213)</td>
      <td>(21212)</td>
      <td>0.021971</td>
      <td>0.562791</td>
      <td>7.270077</td>
    </tr>
    <tr>
      <th>14</th>
      <td>(20726)</td>
      <td>(20728)</td>
      <td>0.026268</td>
      <td>0.440609</td>
      <td>6.488186</td>
    </tr>
    <tr>
      <th>15</th>
      <td>(21977)</td>
      <td>(21212)</td>
      <td>0.024755</td>
      <td>0.490408</td>
      <td>6.335040</td>
    </tr>
    <tr>
      <th>16</th>
      <td>(21928)</td>
      <td>(21931)</td>
      <td>0.020881</td>
      <td>0.438374</td>
      <td>6.303575</td>
    </tr>
    <tr>
      <th>17</th>
      <td>(21929)</td>
      <td>(21931)</td>
      <td>0.021487</td>
      <td>0.421615</td>
      <td>6.062599</td>
    </tr>
    <tr>
      <th>18</th>
      <td>(20727)</td>
      <td>(20728)</td>
      <td>0.030626</td>
      <td>0.411048</td>
      <td>6.052882</td>
    </tr>
    <tr>
      <th>19</th>
      <td>(20728)</td>
      <td>(20727)</td>
      <td>0.030626</td>
      <td>0.450980</td>
      <td>6.052882</td>
    </tr>
    <tr>
      <th>20</th>
      <td>(20726)</td>
      <td>(20727)</td>
      <td>0.026268</td>
      <td>0.440609</td>
      <td>5.913683</td>
    </tr>
    <tr>
      <th>21</th>
      <td>(20726)</td>
      <td>(20725)</td>
      <td>0.031171</td>
      <td>0.522843</td>
      <td>5.686903</td>
    </tr>
    <tr>
      <th>22</th>
      <td>(20727)</td>
      <td>(20725)</td>
      <td>0.037405</td>
      <td>0.502031</td>
      <td>5.460536</td>
    </tr>
    <tr>
      <th>23</th>
      <td>(20725)</td>
      <td>(20727)</td>
      <td>0.037405</td>
      <td>0.406847</td>
      <td>5.460536</td>
    </tr>
    <tr>
      <th>24</th>
      <td>(20728)</td>
      <td>(20725)</td>
      <td>0.032684</td>
      <td>0.481283</td>
      <td>5.234868</td>
    </tr>
  </tbody>
</table>
</div>

  - **Support** : The proportion of transactions that contain both products (antecedents and consequents).  
  - **Confidence** : The probability that a customer will purchase the product in the consequents given that they have already bought the product in the antecedents.  
  - **Lift** : The degree of association between two products. A **lift value greater than 1** indicates that the occurrence of the consequents product is more likely when the antecedents product appears.
    
      **Based on the results of the algorithm, we have the following observations:**
  - (21086) → (21094) and (21094) → (21086) have **a lift of 25.95**, indicating a strong association between these two products. Customers who purchase one of these items have a high probability of buying the other. (21086) → (21094) has **a confidence of 81.83%**, meaning that 81.83% of customers who buy product (21086) will also purchase (21094). (2075) ↔ (20727) has **a support of approximately 3.7%**, meaning 3.7% of all transactions include both products. This suggests that these items are commonly purchased together.
  - Based on the above analysis, businesses can implement cross-selling strategies by suggesting complementary products in the shopping cart or offering discounts when purchasing both strongly associated products. Additionally, creating product bundles with special pricing is an effective way to encourage customers to buy in sets. Notably, products with high lift values should be prioritized in promotional campaigns during major shopping events such as Black Friday or New Year’s sales to maximize revenue.  
- Moreover, businesses can enhance customer experience by integrating product recommendation systems on their websites, such as displaying “Customers who bought this product also bought…” to increase purchase likelihood. Additionally, remarketing campaigns can target customers who have purchased product (21086) but have not yet bought (21094), offering special incentives to drive sales. Overall, applying these strategies will help optimize revenue and improve marketing efficiency based on data-driven insights.
