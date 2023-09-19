<div align = 'center';'><h1>Dairy Sales Analysis</h1></div>
<p><h2>Introduction</h2></p>
<div align='justify';'><p>The dataset provided was sourced from <a href = "https://www.kaggle.com/datasets/suraj520/dairy-goods-sales-dataset">Kaggle</a>. In the dataset, I was provided with various information such as, Farm details on its size, location, and number of cows, Customer Location, and Quantity Sold and in Stock per farm. I have conducted an exploratory data analysis on these different variables and finally done a Time Series Forecasting using XGBoost.  </p>
<h2>Goals:</h2>
<ol>
  <li>Conduct an exploratory data analysis by answering the following questions:</li><br>
    <ul>
      <li>What is the dairy sales trend?</li>
      <li>What are the biggest brands and products based on their revenues, and sales?</li>
      <li>What are the factors for classification of Farm Size?</li>
      <li>Who are the biggest customers based on their buying power</li>
    </ul>
  <br>
  <li>Create a model using Time Series Forecasting through XGBoost that can answer the following questions:</li><br>
    <ul>
      <li>What is the expected sales for the next 20 days?</li>
      <li>What are the most important factors for forecasting?</li>
    </ul>
</ol>
<h2>Summary</h2>
<h2>Extensive Discussion - Exploratory Data Analysis</h2>
<h4>What is the dairy sales trend?</h4>
<p>First I want to see the overall trend of dairy sales. I have created a graph to analyze it easier which can be seen below.</p>
<img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/a019a3d3-9fce-41f0-bebf-4d2d39b46a74"/>
<p>From the graph, I can see that there is no clear overall trend for dairy but however has consistent demand and has some spikes in certain dates. In relation to overall sales, I wanted to see what are the most commonly bought brands, and product.I could easily portray this using a bar chart and also to gauge how far apart the margins are compared to the other different variables.</p>
<h4>What are the biggest brands based on their revenues, and sales?</h4>
<img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/866fca1c-6585-4204-a977-1be2c111c061"/>
<p>Through the graph you can quickly see that the brands Amul, and Mother Dairy are the top 2 most sought of brands and have a significant margin compared to the other brands. If you compare in terms of type of product, Curd has the highest amount of sales but the margin to other products are not that significant. Now I want to dig deeper on this and inspect each brands most selling product.  A graph can be seen below to easily investigate this.</p>
<img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/e292aedb-efea-454b-9f10-756aafcebdcc"/>
<p>From the graph, you can see that even though Amul, and Mother Dairy are the top 2 most sold brands, there are products that they are not the most sought of brand. For example, the brand <strong>Warana</strong> is the brand that has the most sold <strong>Butter products</strong>The main reason why Amul, and Mother Dairy was shows as the top 2 most sought of brand is mainly due to the variety of products that they are selling.</p>
<p>Knowing this, I want to see if there are also differences between in terms of total revenue per brand, and average revenue per order per brand which can be seen below.</p>
<img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/0a492b2c-24a6-4147-b73e-4cf25fe8baef"/>
<p>As expected, both Amul and Mother Dairy are the top Brand earners especially considering their large volume share compared to other brands, however if we will look at the revenue per order, Warana has the highest revenue per order. This means they are selling high value products. In this case, they are the top supplier for Butter products as mentioned earlier.</p>
<h4>What are the factors for classification of Farm Size?</h4>
<p>In the dataset, farms are classified into three different types namely, Large, Medium, Size. I wanted to know what is the main criteria to be classified into one of these types. There are two columns that are initially clearly that would indicate this, Total Land Area, and Number of Cows, thus I have created two box plots that utilizes these two variables.</p>
<img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/0865b25c-9f3d-496a-aaae-bc681f18edfc"/>
<p>From the box plots, you can see that there are no clear differences from the three different Farm Sizes from one another.  This is questionable and I have tried to dig deeper to find possible variables that can indiciate the farm size.  I have wondered maybe it is depending on the brand, but each brand has all types of farm sizes which can be seen below</p>
<p align='center'><img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/24ed5ba5-ef8d-40ad-8e86-e7ab8b592f3e"/></p>
<p> I have explored all possible areas that can indiciate the farm size however, there are no other variables that can indiciate the farm size.</p>
<h4>Who are the biggest customers based on their buying power</h4>
<p> Next I want to see which customers have the highest buying power.  In the dataset, we were only provided with the customer's location.  I have grouped them into each location to see which locations have the highest amount of goods bought. This can be easily done using bar plots as well.</p>
<img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/f9defedb-ead7-4df6-a13c-660811a028c8"/>
<p>I have created two bar plots showing which locations has the highest monetary amount, and the highest quantity amount. From here you could see that Chandigarh has the highest monetary amount of goods sold, while Delhi has the highest quantity amount.</p>

<h2>Extensive Discussion - Time Series Forecasting</h2>


</div>
