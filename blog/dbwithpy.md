# Database with python
Database about menu
Database with python using pandas and sqlite
``` python
from flask import Flask
from flask_sqlalchemy import SQLAlchemy
from flask import Flask , render_template, jsonify, request, redirect, url_for, jsonify
import pandas as pd

```
and create data in .csv file
``` csv
Menu,Price,Category,Description
Ramen Noodle,50 Bath,Ramen,Ramen Noodle
Salmon Sushi,20 Bath,Sushi,sushi
Tuma sushi,15 Bath,Sushi,sushi
Curry rice,80 Bath,rice,curry rice
Fish with rice,50 Bath,rice,fish with rice
Noodle with tempura,120 Bath,Ramen,Noodle with tempura
```
and create database with
``` python
market_list = pd.read_csv("filename.csv")

app = Flask(__name__)
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///app.db'
app.config['SQLALCHEMY_TRACK_MODIFICATIONS'] = False
db = SQLAlchemy(app)


class MarketData(db.Model):
    menu = db.Column(db.String(20), primary_key=True)
    price = db.Column(db.Integer, nullable=False)
    category = db.Column(db.String(15), nullable=False)
    description = db.Column(db.String(100), nullable=False)
    def __init__(self, menu, price, category, description):
        self.menu = menu
        self.price = price
        self.category = category
        self.description = description

db.create_all()
```
also show data on .html file
``` html
{% for market in market_db %}
Name : <p>{{market.menu}}</p> <br>
Price : <p>{{market.price}}</p> <br>
Category : <p>{{market.category}}</p> <br>
Description : <p>{{market.desription}}</p>
{% endfor %}
```

to run use `python app.py` you will get `http://127.0.0.1:5000/`

### File
template
 - index.html
 - product.html
 
app.py 
data.csv (data file)

app.db (data base file)


(14/8/2021 10:24 AM)
