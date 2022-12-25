# News and Political Affiliation

Project with:
- An example of modeling corruption data based on political party affiliation. Uses pandas, keras and scikit-learn.
- Scraping of political news with people and their positions on sentences highlighted. Uses Selenium and huggingfaces.

Breakdown of each notebook:

"0__Baixar_arquivos_do_TSE.ipynb":
  - Downloads zip files with political affiliation data from TSE using wget.

"1__Carregamento_de_Dados.ipynb":
  - Cleans political affiliation data.
  - Downloads corruption data from CEAF and cleans it. 
  - Links affiliated with corrupts with approximate merging.

"2__Atributos_e_Modelagem.ipynb":
  - Performs feature engineering (including imputation and balancing data) and train-test splitting. 
  - Compares neural network trained in Keras with Random Forest trained with scikit-learn. 
  - Neural network obtained AUC of 0.789 on the test dataset.

"3__Leitura_de_noticias.ipynb":
  - Scrapes data from news website related to politics using Selenium, requests and BeautifulSoup.
  - Loads a pre-trained NER model from HuggingFaces library.
  - For each news page, gets people/entities in the text by runnning NER, shows the sentence with each person highlighted.
  - Also shows wordcloud of content.
