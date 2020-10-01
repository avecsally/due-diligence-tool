# GWU & ABC NYC
## Due Diligence and Risk Rating Tool
Ansheng Huang, Haoyun Peng, Huang-Chin Yen, Jianing Zhang, Yike Liu


## Abstract 

 
Banks like our client, Agricultural Bank of China (ABC bank), have the need to conduct due diligence for their customers to avoid potential risk. Traditional due diligence work is often done manually, and it is very time consuming. Therefore, ABC bank is hoping that we can develop an interactive tool to help them use Machine Learning and Artificial Intelligence algorithms to conduct the due diligence job and present the final results for human intervention. This tool will ask for potential customers’ names, more in need, social security numbers, and nationalities. Then the tool automatically searches the background and information of their potential customers on Google. Also, information will update automatically and timely on a daily basis. Finally, the tool will show the top 10 keywords associated with this potential customer and the links of articles that contain these 10 keywords. However, the tool does not need to have ratings function. Once our tool generates the information, ABC bank will evaluate and determine whether to deal with potential customers or not internally.
 
## Data Preparation
 
- Entity Attributes: There are several types of data that are required in conducting the Due Diligence Tool. First, Entity Attributes are required to complete the search. The content of the Entity Attributes include: Name (required), nationality (not required), age (not required), and etc.. Since banks are protective of their clients information, there is no guarantee that any further information will be provided, but those optional entity attributes will definitely be helpful in conducting a more precise search. 
 
- Search Results: Once the search results are generated, those articles will be saved into txt files for further natural language processing analysis. Each article will be saved into a single file. 
 
- Sensitive Words: There are two categories of sensitive words in this project: Financial Crime Related Terms and Sanction List. Our client will be providing us a list of words that contain those highly related to potential defamation for the bank, for example: Fraud, Money Laundry, Financial Crime and etc.. Our client also wants to monitor the customers’ activity to see whether there is a sanction violation. There are certain countries that are banned to have any financial activity with the U.S., such as Cuba, North Korea. The list of names and countries is also required to conduct the search. The list of words is stored in an excel file. 
 
- Sensitive Analysis Stopwords: When conducting the sensitive analysis, a list of stop words is required to finish the process. The list of stop words will include the sentiments or so called identifier to identify the sentiment of an article. 

## Methodology

The method we will be taking to finish the tool build up will be separated into three parts. While Part I and Part II have similar functions, we will be focusing on the Part I algorithm build up and dashboard design in the first place. 
In order to complete the Part I functionalities, Web Scraping will first be used to get the results from public search engines, the results will be saved into txt files. Then Topical Analysis will be conducted after finding the top 100 articles to match the sensitive words. The results will include a summary for all top 100 articles and we will only be using the top 10 results. The move further, Sentiment Analysis will be used to identify the sentiment for those articles. The summary reports will be displayed on the dashboard to help the user have a more precise sense of the summary. 

## Deployment

#### Goal: 
Build a Due Diligence and Risk Rating Tool for the Department of Compliance Analytics in the Agricultural Bank of China. 

#### Functionality: 
The function of the tool will have two main parts which described as following: 


### Part I: A Random Customer Risk Rating Dashboard

- Target Entity

The interactive dashboard that requires a data entry- which is the target customer’s name along with optional detailed information such as Date of Birth, Company, Country and etc. if it is available. 
- Due Diligence Search

Once we have the target customer’s name, the tool will conduct the search through Google and present the most relevant articles of that target person ordered by the date of its’ publish from latest to earlier articles.  Once the articles are identified, a Natural Language Processing Sentiment Analysis will then be conducted to extract the Keywords from the article using a predefined Stopword List. The Stopword List contains a negative list of words that are categorized by the Risk Department of those Financial Crime related vocabularies such as: Fraud, Money Landry, Financial Crime and etc.. 
The keywords will be extracted and count the occurrence in that article then presented as the result listed alongside the articles’ link. 
With those information listed on the dashboard, the Risk Management Team can then determine the level of risk regarding the final results presented. 


### Part II: Constant Monetization on Certain Customers 

- Target Customers Monetization

This portion of the Due Diligence and Risk Rating Tool have a group of predefined target customers. The names for the group of people will appear in a dropdown menu. 

- Time Range Selection

Users then also have the option to select a certain period of time range. For example, show articles related to this person in the past week, or past month. 

- Constant Due Diligence Searching

The tool will provide the search results for each individual on the name list using a similar algorithm mentioned in Part I. First search through the internet of related articles for the target customer, then display the counted occurrence of those keywords listed in the Stopword List. 
The research results will be displayed on the interactive dashboard, and the Users have the option to click on the resources and investigate the credibility of the information to decide the level of risk for that customer. 
Our team and client have made an accordance to focus on Part I in the first place and see how it works. If few of the functionality can not be satisfied, we then would probably drop Part II. Since Due Diligence is such a complex field and does require lots of human research, which makes it impossible to count on Machine Learning and Artificial Intelligence algorithms fully. Knowing the present of those obstacles, we will be focusing on the first part of the functionality and hope we can reach our expectation. 


