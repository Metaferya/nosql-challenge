# Eat Safe, Love
## Notebook Set Up
## Import Dependencies

from pymongo import MongoClient
import pandas as pd
from pprint import pprint

# Create Database Instance

# Create an instance of MongoClient
mongo = MongoClient(port=27017)

# Assign the uk_food database to a variable name
db = mongo['uk_food']

# Review the collections in our database
print(db.list_collection_names())
# Output: ['establishments']

# Assign the collection to a variable
establishments = db['establishments']


