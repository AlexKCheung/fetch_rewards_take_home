# Fetch Rewards take home assignment
https://github.com/fetch-rewards/receipt-processor-challenge 


## HOW TO RUN: 
### Make sure you have flask, by using this command: pip install Flask  
### One: run the program 
python3 app.py  

### Two: in terminal, send the POST via curl
Two Methods: either via sending a json file or manually typing the whole json out

curl -X POST http://localhost:5000/receipts/process -H "Content-Type: application/json" --data /morning-receipt.json


curl -X POST http://localhost:5000/receipts/process -H   
"Content-Type: application/json" --data '{  
  "retailer": "Target",  
  "purchaseDate": "2022-01-01",  
  "purchaseTime": "13:01",  
  "items": [  
    {  
      "shortDescription": "Mountain Dew 12PK",  
      "price": "6.49"  
    },{  
      "shortDescription": "Emils Cheese Pizza",  
      "price": "12.25"  
    },{  
      "shortDescription": "Knorr Creamy Chicken",  
      "price": "1.26"  
    },{  
      "shortDescription": "Doritos Nacho Cheese",  
      "price": "3.35"  
    },{  
      "shortDescription": "   Klarbrunn 12-PK 12 FL OZ  ",  
      "price": "12.00"  
    }  
  ],  
  "total": "35.35"  
}'  

### This returns an id which you then copy paste into the GET endpoint
curl http://localhost:5000/receipts/COPY_PASTE_THE_ID_HERE/points

