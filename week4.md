
## **Week 3: Text mining and Named entity recognition**

This week focused on enhancing the system developed in Week 3. The major improvements aimed to address data collection, consistency, and visualization by refining the web crawling process, improving data extraction techniques, comparing different language versions, and packaging the project for future use

### New enhancements:

#### 1. Data Collection:
a. Data Collected from Mathaf Encyclopedia
I updated the code to successfully scrape all content in the webpage by specifying a start phrase and end phrase, which made it cusotmizable for each website. A "stop phrase" parameter was added, enabling the script to stop extracting content once a specific phrase (e.g., "By visiting this website, viewing, accessing or otherwise using" for Mathaf) is encountered.
The script was also modified to identify and scrape both English and Arabic biographies.
This involved detecting language-specific URLs ("/en/" vs. "/ar/") and adapting the scraping to extract data from both versions.


#### 2. Named Entity Recognition
To accommodate the differences in content across the websites, we used distinct entity label lists for each site. Specifically, we tailored the Named Entity Recognition (NER) model to recognize and classify entities relevant to the Mathaf Encyclopedia and QM’s Online Collection, as their biographical data and contexts differed. As a result, each website's data was processed with a customized set of entity labels to ensure accurate and context-specific entity identification.


#### 3. Combining Results into a Single CSV
In addition to the individual CSV files for each page, a single CSV was created to store aggregated data, including URLs, entities, and their frequencies for both English and Arabic versions.
![image](https://github.com/user-attachments/assets/5eff5753-33b3-4f05-8eaa-79ad2ee7f8b4)



#### 4. User-Configurable
users are allowed to specify their extraction preferences by specifying the following choices:
  1- the type of website if it is an encyclopedia or collection
  2- if they prefere to crawl the whole website or just a singl web page
  3- if they chose to crawl the whole website then they can specify the path they would like to crawl
  4- specifying the start phrase and end phrase of the content they want to scrape
![image](https://github.com/user-attachments/assets/adee0dc1-d7e8-440a-b94d-3b3963a0e760)

  

#### 5. interactive visualization
graph-based tools such as D3.js were used to reveal connections between different entities found in each webpage. these visualizations could allow users to filter entities, and explore the relationships between different artists.

![image](https://github.com/user-attachments/assets/5f7a2ce3-6676-4a4e-9163-7800c6217a19)



The project has moved from basic data extraction to meaningful visualization, helping museums make better use of their vast textual resources. By cmbining automation, entity recognition, and interactive graphs, this tooll might enhance hoow histor is curated, studied an shared with the world.

link to github repo: [https://github.com/Leen-QM/web-scrapping-tool/blob/main/README.md](https://github.com/Leen-QM/web-scrapping-tool/tree/main)

