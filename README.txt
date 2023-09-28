# Project Description
This repository contains items from the paper "Construction and Consumption of FAQ Knowledge Graphs in the E-Commerce Domain".

## Files' and Folders' Description 

dataset.csv: Contains all entities and metadata used in KG creation and consumption, scraped from Tokopedia's FAQ page per February 29th 2023
knowledgegraph.ttl: The constructed Knowledge Graph 
apache-jena-fuseki-4.7.0: Folder containing the Apache Jena Application to run the SPARQL queries. For further guides, see below
SPARQL queries: Folder containing 10 SPARQL queries that can be run using Apache Jena Fuseki.

## How to open Apache Jena Fuseki to run SPARQL queries

On MacOS:
1. Open the "Terminal" application and run the following command:
cd <path to the folder apache-jena-fuseki-4.7.0>

2. Run the following command:
/Applications/apache-jena-fuseki-4.7.0/fuseki-server --update --mem /ds

3. Wait until you see the line that looks like this:
<time> INFO  Server          :: Started <date> <time> <timezone> on port 3030

4. Open a web browser (such as Google Chrome) and write "localhost:3030" on the URL

## How to use Apache Jena Fuseki to run SPARQL queries
1. The first thing to do is to add the knowledge graph into the database. On the navigation bar on top of the screen, click on "datasets". Then, fill in the field of "Dataset name" to anything (preferably "knowledgegraph") and also choose persistent for "Dataset type". Click on "create dataset" button.
2. The next step is to add the data. After creating a new dataset, you will be redirected to the "existing datasets" section. Under the "actions" column, click the button "add data". Then, click on the button "select files" and choose the knowledgegraph.ttl file. Click on the button "upload now" under the "actions" column.
3. The next step is to query. Click on the "query" button on the far left, or if you struggle find it, go to this URL:
http://localhost:3030/#/dataset/knowledgegraph/query
4. Type in the SPARQL query and click on the run button on the far right of the text field (the button looks like a sideways triangle)

