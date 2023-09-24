<div align = 'center';'><h1>Covid Data Analysis</h1></div>
<p><h2>Introduction</h2></p>
<div align='justify';'><p>The dataset provided was sourced from various Wikipedia websites. This project is slightly different from the rest as I wanted to work on a new sets of Python Tools like webscraping to gather my own data. I will also explain in detail the processes, and challenges I faced throughout my webscraping project and how I handled it. I did webscraping to extract two types of data, firstly a statistics on Covid 19 in different countries, and secondly each country's Human Development Index (HDI) from the United Nations which shows whether a categorizes country's development. </p>
<h2>Goals:</h2>
<p>The goals of this project are as follows:</p>
<ol>
  <li>Create my own dataset from webscraping Wikipedia websites on Covid19 statistics, and HDI per country</li>
  <li>Clean my dataset to analyze and get insights</li>
  <li>Find relationships between the development of the country and its affect on Covid19 Cases and deaths</li>
</ol>
<h2>Summary</h2>
<p>In this project, I was able to extract, and cleaned my data from Webscraping Covid 19 Statistics, and HDI for several countries. I was able to create my own dataset through this project and was able to clean and ensure that all data types are consistent with one another. Furthermore, I was able to relate if you will perform better in mitigating Covid19 deaths if you are from a developed country or not. Overall, this is a very logical assumption to have especially highly developed countries have better infrastructure compared to developing countries however I wanted to see if there is a significant difference from one another. In this study, I was able to conclude that each type of development category were different from one another especially on the percentage of dying from Covid.</p>
<h2>Extended Discussion</h2>
<h3>Extracting the Data</h3>
<p><h4>Covid Statistics</h4>Firstly, I used <a href = "https://en.wikipedia.org/wiki/COVID-19_pandemic_by_country_and_territory">this Wikipedia page</a>as my source. The table that I will be extracting is this:</p>
<img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/fa408ce1-4c54-4999-8349-813e00276cfe"/>
<p>I will be using <em>BeautifulSoup</em> library to be able to easily extract this. There are several tables in the website, the table I am looking for specifically is number 12. Knowing this, I will be extracting the headers of the table through the code below:</p>
<img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/73770fba-1ec6-4000-a1b6-55ebb936fbb6"/>
<p>Upon further inspection, Country list are also listed as a table header, this was an issue at first, however it is easily remedied through finding its class or scope.  I was able to extract the country names through the functions below:</p>
<img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/8d24b00d-2a16-442a-a77b-6b1df8f02346"/)
<p>Next I was able to extract each row data through this function:</p>
<img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/6af4730c-bcbf-4e99-b96c-7c816744e2d7"/>
<p>Once I have done this, I am now able to create my DataFrame and had to do a little bit of cleaning with data through the functions below. The final DataFrame for the Covid Statistics can also be seen below</p>
<img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/07e6b958-4694-4a13-b06d-b1c96c42522c"/>
<p>Issues found during the cleaning process:</p>
<ol>
  <li> A datarow of European Union which is just the sum of the countries within the Union even if they are already included in the list</li>
  <li> The Country <em>China</em> is listed as China[b]</li>
  <li> Change rows to numeric values to be able to be used for analysis</li>
</ol>
<p><h4>HDI per Country</h4></p>
<p>A brief introduction about HDI or the Human Development Index.  The index considers the health, education, and income in the country to give a measure of human development that allows to be comparable to per country.  The source I used for this dataset can be seen from <a href= "https://en.wikipedia.org/wiki/List_of_countries_by_Human_Development_Index">this Wikipedia page</a>In a similar process earlier, I used Beautiful Soup to extract the necessary data. I also experienced a few problems here and I have listed them below:</p>
<ol>
  <li> Country names are also listed as headers however it does not have class or scope indicated in its object however it is easily indexed through the function below</li>
  <img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/a743e1e3-6261-46a3-a537-c7b14bce6fe4"/>
  <li> There are merged rows in the table which I was able to handle in the highlighted codes below</li>
  <img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/8e526094-0560-4eb6-8384-3263aa027df2"/>
</ol>
<p>I also have to classify these HDI into four categories from the standard of the United Nations who compiles these statistics.</p>
<table align="center";>
  <tr>
    <th>Category</th>
    <th>HDI Range</th>
  </tr>
  <tr>
    <td>Low</td>
    <td>HDI<=0.550</td>
  </tr>
  <tr>
    <td>Medium</td>
    <td>HDI > 0.500 and <=0.699 </td>
  </tr>
  <tr>
    <td>High</td>
    <td>HDI > 0.699 and <=0.799 </td>
  </tr>
  <tr>
    <td>Very High</td>
    <td>HDI >0.799 </td>
  </tr>
</table>
<p>Once this is done you can see the final dataframe for HDI below:</p>
<img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/d328dffc-9cb7-45ae-b97c-90f943ec542a"/>
<h4>Analysis on the dataset</h4>
<p>I merged the two datasets based on the Country name.  I have used the HDI dataset as my main table as this has fewer list of countries than the COVID 19 statistics tables. I have added 3 columns. First is the population column which can be derived from dividing Deaths column with Deaths per Million column. Second is the Percentage of Cases based from the Population.  This just shows the percentage of cases from the population.  Finally, Death Percentage of Cases this just shows from the Total number of cases, how many percent have died.</p>
<h5>What are the top 10 highest Case Percetage from Population, deaths per million, Percentage Death per Case</h5>
<img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/89236536-2079-43fd-8445-9697a99f5acd"/>
<p>From the graphs above, you could easily see which countries that were most affected from Covid and it is a mixture of developed and developing countries. Next I want to see are there any clear difference from each category of Human Development</p>
<h5>Is there a significant difference between the 4 different human development categories from the effects of Covid?</h5>
<img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/77e609c6-b482-4314-8e9a-eab6cb004504"/>
<p>I could easily determine this using the boxplot graph. If the median per category is outside the body of the other categories, it can indiciate that they are statisticailly different. The Percentage of Cases, and Deaths per Million box plots can show each category type is significantly different from one another. You could also see that Very High Developed countries had higher averages compared to other countries. My main hypothesis in this is because Very High Developed countries might have smaller population sizes compared to other countries. This can inflate these values as these were based from the population. On the third box plot, however, very high developed countries have the lowest death percentage from cases as this may indicate they have a more established healthcare system as compared to low developed countries. </p>
<p>Next I want to see if my hypothesis is correct from the bar graph below.  You can see that Very high developed countries indeed have the lowest average population per category.  This may cause the values that I mentioned earlier to inflate.</p>
<img src="https://github.com/ibpinto3098/Personal-Projects/assets/144035560/2a013b6a-2586-4a5b-b67d-24bb4926b894"/>
<h4>Conclusion</h4>
<p>From this analysis you can see that highly developed countries did in fact perform better compared to low and medium developed countries especially in regards to the chance of dying from getting contacted of the disease. This indicates that these highly developed countries have the necessary facilities and programs to control and stabilize the situation as compared to developing countries.</p>
</div>

