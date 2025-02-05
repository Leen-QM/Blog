## Week 3: Text Mining and Named Entity Recognition

This week focused on enhancing the system developed in Week 3. The major improvements aimed to address data collection, consistency, and visualization by refining the web crawling process, improving data extraction techniques, comparing different language versions, and packaging the project for future use.

### New enhancements:

#### 1. Data Collection:
The code was updated to effectively scrape the entire webpage by specifying both a start and end phrase, making the process customizable for each website. A "stop phrase" parameter was introduced, allowing the script to halt content extraction once a designated phrase (e.g., "By visiting this website") is encountered. Additionally, the script was modified to recognize and scrape biographies in both English and Arabic. This involved detecting language-specific URLs ("/en/" for English and "/ar/" for Arabic) and adapting the scraping process accordingly to handle both versions.


#### 2. Named Entity Recognition
To accommodate the differences in content across the websites, we created separate entity label lists for each. We specifically modified the Named Entity Recognition (NER) model to recognize and classify entities relevant to the Mathaf Encyclopedia and QM's Online Collection, as their biographical data and contexts differed. As a result, each website's data was processed with a customized set of entity labels to ensure accurate and context-specific entity identification.


#### 3. Combining Results into a Single CSV
In addition to the individual CSV files for each page, a single CSV was created to store aggregated data, including URLs, entities, and their frequencies for both English and Arabic versions.
![image](https://github.com/user-attachments/assets/5eff5753-33b3-4f05-8eaa-79ad2ee7f8b4)



#### 4. User-Configurable
Users are allowed to specify their extraction preferences by specifying the following choices:

![image](https://github.com/user-attachments/assets/adee0dc1-d7e8-440a-b94d-3b3963a0e760)

  

#### 5. Interactive Visualization
Graph-based tools such as D3.js were used to reveal connections between different entities found in each webpage. These visualizations could allow users to filter entities and explore the relationships between different artists.

![image](https://github.com/user-attachments/assets/5f7a2ce3-6676-4a4e-9163-7800c6217a19)


The project has moved from basic data extraction to meaningful visualization, helping museums make better use of their vast textual resources. By combining automation, entity recognition, and interactive graphs, this tool might enhance how history is curated, studied, and shared with the world.

link to Webscrapping tool: [https://github.com/Leen-QM/web-scrapping-tool/blob/main/README.md](https://github.com/Leen-QM/web-scrapping-tool/tree/main)

