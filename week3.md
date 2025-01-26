
## **Week 3: Text mining and Named entity recognition**

This week was focused on exploring text mining techniques and implementing Named Entity Recognition (NER) to analyze and extract valuable information from museum encyclopedias. I have aimed to develop a system for identifying, counting, and visualizing entities in a word cloud. The task also involves extending this approach to multiple URLs.

### The task was devided into the following steps:

#### Web Crawling
The fisrt step was to implement a web crawler that navigates through the base URL and collect all the biography subpages that contain `/bios/Pages` in their URL. Using two python libraries such as "requests" and "BeautifulSoup", I was able to identify all the relevant URLs that Contiain artists Biographies.
![image](https://github.com/user-attachments/assets/5c33be3c-4bb9-4bd5-9cd8-64be91e9d252)


#### Web Scrapping
The next step was to scrape the collected web pages for biography content and clean the HTML code extracted from these webpages. The main challenge in this step was the inconsistent HTML structure across different pages, which made it harder to bound the biography between two HTML tags. To solve this, I decided to locate and extract text placed between two H1 headers which are "Biography" and "Exhibitions".


#### Named Entity Recognition
After scraping the  biography content, i used the GLiNER model - which is a pre-trained multilangual model for extracting named entities- to identify and classify the biography into multiple entity labels such as: People names, countries, and dates.


#### Data Analysis
Once the entities were correctly identified, I exported the data into a table that included the entity type and the count of occurrences. A CSV file was created for each webpage and which contained: 
- the URL of the webpage
- the identified entities
- entity labels
- the frequency of each entity across the webpage

![image](https://github.com/user-attachments/assets/67ac5c51-855d-4805-a4c2-8b1c32f1b832)


#### Data Visualizing
After cleaning the data, I was able to present it using the "WordCloud' library to generate a word cloud for each webpage. The library extracted the entities and their frequencies from the CSV files and created word clouds that highlighted the most frequent words.

![image](https://github.com/user-attachments/assets/0154e571-8935-4873-a3aa-f175cd21d453)



This week, I got hands-on experience with web crawling and scraping in Python. I also learned how to deal with inconsistencies in data and extract good insights using NER. I was able to successfully analyse and present the retrieved information by grouping the items into structured data and creating graphics such as word clouds.


