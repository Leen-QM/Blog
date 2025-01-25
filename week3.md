
---
layout: default
title: week 2
description: This is just another page
---

## **Week 3: Text mining and Named entity recognition**

This week was focused on exploring text mining techniques and implementing Named Entity Recognition (NER) to analyze and extract valuable information from museum encyclopedias. I have aimed to develop a system for identifying, counting, and visualizing entities in a word cloud. The task also involves extending this approach to multiple URLs or entire directories.

### The task was devided into the following steps:

#### Web Crawling
The fisrt step was to implement a web crawler that navigates through the base URL and collect all the biography subpages that contain `/bios/Pages` in their URL. Using two python libraries such as "requests" and "BeautifulSoup", I was able to identify all the relevant URLs that Contiain artists Biographies.

(image)


#### Web Scrapping
The next step was to scrape the collected web pages for biography content and clean the HTML code extracted from these webpages. The main challenge in this step was the inconsistent HTML structure across different pages, which made it harder to bound the biography between two HTML tags. To solve this, I decided to locate and extract text placed between two H1 headers which are "Biography" and "Exhibitions".

(image)

#### Named Entity Recognition
After scraping the  biography content, i used the GLiNER model - which is a pre-trained multilangual model for extracting named entities- to identify and classify the biography into multiple entity labels such as: People names, countries, and dates.

(image)

#### Data Analysis
Once the entities were correctly identified,  I exported the data into a table that included the entity type and the count of occurrences. A CSV file was created for each webpage and which contained: 
- the URL of the webpage
- the identified entites
- entity labels
- the frequency of each entity across the webpage

  (image)

#### Data Visualizing
After cleaning the data, I was able to present it using "WordVloud' library to generate a word cloud for each webpage. The library extracted the entities and their frequencies from the CSV files and created word clouds that highlighted the most frequent words.

(Image)

This week, I learned the importance of text preprocessing and the role of stemming and stop words in NER. Initially, I thought that text could be directly analyzed for entities, but I realized that cleaning and structuring the data is essential for accurate results. By processing the text and organizing the entities, I was able to create clearer visualizations that showed meaningful insights about the document's content. I also discovered the power of Python libraries like spaCy for automating the extraction of named entities, which greatly sped up the process.


This week, I gained practical experience in web crawling and web scraping using Python. I also learned how to handle inconsistent data and extract valuable insights using NER. By organizing the entities into structured data and generating visualizations, I was able to effectively analyze and present the extracted information. The process highlighted the importance of clean data extraction, proper entity categorization, and the role of custom functions in improving the accuracy of entity recognition.


