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

The code only has to be run, it doesn't ask for any input.
You will see comments on the code with explanations of what is being done.