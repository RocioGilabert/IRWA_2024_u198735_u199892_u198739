**GROUP_101_3**
* Rocío Gilabert u198739
* Laura Juan     u199892
* Elena Barrio   u198735

## Part 1: Text Processing and Exploratory Data Analysis
The code for the first part of the project is structured in the follwoing way:
1. **Imports:** This section contains all the imports that are necessary for the code to run properly. Run this section before running the rest of the sections.
   This section also includes the necessary cell to connect to you Google Drive, were you must have the necessary data.
2. **Functions:** This section contains the functions that are necessary to clean the tweets. All of them are commented in the .ipynb file and explained in detail in the pdf.
   Run all this section 
3. **Load Information:** In this section we load the data of the json and the csv files. In the first cell of this section you will observe that we have loaded the data from our drive,
   so you have to copy and paste files paths. The path to *farmers-protest-tweets.json* has to be loaded into *json_path* and the path to *tweet_document_ids_map.csv* has to be loaded into *csv_path*.
   Run all this section after adding your paths.
4. **Clean Tweets:** In this section we process the tweets and create the dictionary that we will use in the followimng sections
5. **Exploratory Data Analysis:** Here we implement the different analysis that we performed.


## Part 2: Indexing & Evaluation
1. **Indexing:** In this section we started implementing the required functions to create a non-score based index: create_index(...) and search(...). The first one creates the index and the second one allows us to search it. You can test that it works by uncommenting the cell that follows the search(...) one. It will ask for an input and it returns 10 documents that contain, at least, one query term. The index must be created by calling the create_index(...) function. It will be done automatically if the code is runned sequentially. 
	Next step is to create a score based index. We do so by implementing a create_index_tfidf(...) function, which creates a index based on tf-idf weights. rank_documents(...) and search_tf_idf(...) functions are necessary too for this new type of index. Again, you can test that it works by uncommenting the next cell. It will ask for a query and it will return the top-10 ranked tweets matching that query, as well as their score. 
2. **Evaluation:** Here we start by creating a dataframe with the prediction scores of each of the documents (evaluation_gt.csv file). Additionally, there will be a column for the label and predicted scores for each query. For each document we then fill this information. Next step is to define the evaluation techniques functions. For each query we then fill its prediction_score for its corresponding query. The other prediction_scores will be 0. Finally, we are able to call the evaluation metrics functions and we get the results. Next step is to compute the metrics for our own queries and ground truths. To this end, we open our ground truth .csv file and we randomly fill the rows that are irrelevant documents, making sure that those documents haven't yet appeared in the dataframe. The following steps are the sames than before: create new columns for each different query, fill them with their corresponding values and call the evaluation metric functions to get the results. The end of this section is the 2-dimensional representation of the returned tweets of the five queries we defined.

## Part 3: Ranking
1. **Functions:** In this section we only have the funcion to compute the min max scaling to normalize the different properties that we took into account to compute the popularity for our score.
2. **TF-IDF + Cosine Similarity:** Here we have the tf-idf function improved after the feedback received from part 2. We have added the cosine similarity as explained in the report. Also, we have an example of usage with a query.
3. **Our score + Cosine Similarity:** Here we have the function to compute our socre + cosine similarity based on our criteria explained also in the pdf report. We have also added an example of usage of this function with the same query as in the tf-idf + cosine similarity
4. **BM25:** In this section we have implemented the BM25 ranking method. We have also added an example of usage of this function with the same query as in the other rankings.
5. **Top20 List of Documents:** Here we implement the word2vec + cosine similarity and, then, we have retrieved for each of our 5 queries from part 2 their top 20 list of documents with its tweet id, the score and the content.
6. **Extras:** We have added two sections with extras. In the first section you will find the implementation of sentence2vec + cosine similarity and the output for the query 'indian government'. Then, in the second section, you will find the implementation of doc2vec + cosine similarity and the output for the query 'indian government' also.

## Part 4: User Interface and Web Analytics
1. **User Interface:** In this first part we developed the search engine of the web app. First, we integrated our search algorithms to be able to use them in the web app, then we loaded the .json file as corpus and edited the functions in search_engine.py. Finally, we edited a bit the results.html and doc_details.html as needed to show the tweets as we desired
2. **Evaluation:** In this section we have collected some data during the use of the web app in different spots and, with that information, we developed the stats and the dashboard sections of the project.
For this part of the project you need to add the 'farmers-protest-tweets.json' file into the folder 'IRWA-2024-u198735-u199892-u198739-part-4-app' to be able to run the app. Also, in case you need it, you should create a Python environment and import the libraries needed. The last step is to write 'python web_app.py' to run the code. It may take a bit to load, but be pacient please! We promise that it will be worth it 😊.  
You will see comments on the code with some explanations of what is being done.
