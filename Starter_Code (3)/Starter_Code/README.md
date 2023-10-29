# nosql-challenge
Module_12_challenge
# nosql-challenge:

Leveraging information sourced from the **UK Food Standards Agency** establish a NoSQL database in MongoDB, import the dataset, and employ the PyMongo module to accomplish further tasks.

The challenge is split into three sections:


* Establish the database, establish a connection to both the database and collection within a Jupyter Notebook.
 *  Modify specific records and fields within the database collection. 
 * Conduct exploratory analysis on the documents present in the database.

 ## Database and Collection Creation:
 Create, and import the data into, the database. Followed by connecting to the MongoDB a Jupyter Notebook and PyMongo:
 * Using the **establishments.json** data file provided, use the 'mongoimport' function in a terminal to create a database named 'uk-food' and a collection 'establishments' to import the documents.
    - **mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json**

 * In a jupyter notebook, import the required libraries
* PyMongo
* Pretty Print (pprint)
* Create an instance of the Mongo Client.
* Confirm that you created the database and loaded the data properly:
* List the databases you have in MongoDB. Confirm that 'uk_food' is listed.
* List the collection(s) in the database to ensure that 'establishments' is there.
* Find and display one document in the establishments collection using 'find_one' and display with 'pprint'.
* Assign the 'establishments' collection to a variable to prepare the collection for use.

# Update Documents and Field Datatypes:
In the previously generated Jupyter Notebook, create the code to insert a new document, modify fields, remove unnecessary documents, and change the data types of specific fields.
* Add a new document for a recently opened restaraunt using the following data

![distionary for newly opened restaurent data]("C:\Users\bella\Desktop\nosql-challenge\Starter_Code (3)\Starter_Code\dictionary_for_new_restaurents_data.png")
* Retrieve the **'BusinessTypeID'** for **"Restaurant/Cafe/Canteen"** and display only the **'BusinessTypeID'** and **'BusinessType'** fields. 
* Update the information for the new restaurant with the obtained **'BusinessTypeID'**. The magazine has no interest in establishments in **"Dover"**, so ascertain the number of documents containing the **"Dover"** Local Authority. Remove any establishments within the **"Dover"** Local Authority from the database, and verify the count of documents to ensure their deletion. Rectify the data type issue by using 
**'update_many'** to convert number values stored as strings to actual numbers for **'latitude'** and **'longitude'**. Finally, use **'update_many'** to convert **'RatingValue'** to integer numbers.



-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Exploratory Analysis:
With the database documents prepared, conduct some exploratory analysis on the database to provide some high level insights:
For each question, provide the following information, unless stated otherwise (visible within the jupyter notebook):
*  Use 'count_documents' to display the number of documents contained in the result.
    - Display the first document in the results using 'pprint'.
    - Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.
* Which establishments have a hygiene score equal to 20?
* Which establishments in "London" have a 'RatingValue' greater than or equal to 4?
* What are the top 5 establishments with a 'RatingValue' of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
* How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.

* all in CSV_output folder

