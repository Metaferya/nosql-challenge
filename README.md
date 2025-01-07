# Eat Safe, Love
## Notebook Set Up
## Import Dependencies

from pymongo import MongoClient

import pandas as pd

from pprint import pprint

## Create Database Instance

+ Create an instance of MongoClient

  mongo = MongoClient(port=27017)

+ Assign the uk_food database to a variable name

  db = mongo['uk_food']

+ Review the collections in our database

  print(db.list_collection_names())

+ Assign the collection to a variable

  establishments = db['establishments']

# Part 1: Database and Jupyter Notebook Set Up
## Import the Data
Import the data provided in the establishments.json file from your Terminal. Name the database uk_food and the collection establishments.

### Command:

mongoimport --db uk_food --collection establishments --file establishments.json --jsonArray

## Dependencies

from pymongo import MongoClient

from pprint import pprint

## Create Database

+ Create an instance of MongoClient

  mongo = MongoClient(port=27017)

+ Confirm that our new database was created

  print(mongo.list_database_names())
  
#### Output: ['Artifacts', 'Customers', 'EPA', 'Mechanics', 'admin', 'classDB', 'config', 'local', 'travel_db', 'uk_food']

+ Assign the uk_food database to a variable name

  db = mongo['uk_food']

+ Review the collections in our new database

  print(db.list_collection_names())
  
#### Output: ['establishments']

+ Review a document in the establishments collection

  pprint(db['establishments'].find_one())





