# Brands

## Get All Brands

```ruby
require 'raise_api'

api = Raise::APIClient.authorize!('user')
api.brands.get
```

```python
import raise_api

api = raise_api.authorize('user')
api.brands.get()
```

```shell
curl "https://api.raise.com/commerce/v1/brands"
  -H "Authorization: user"
```

```javascript
const api = require('raise_api');

let api_client = api.authorize('user');
let brands = api_client.brands.get();
```

> The above command returns JSON structured like this:

```json
{
 "brands": [{
     "circle_icon_url": "https://s3.amazonaws.com/raise-content/ibi/TGIFridays-Logo.png",
     "brand_uuid": "7c3521e5-bda6-4216-a72a-bbb8d910866f",
     "instant_config": {
       "min_value": 0,
       "disclaimer": "Redeemable In Restaurant Only. Write card number on back of printed check.",
       "denominations": [
         2500,
         5000
       ],
       "increment": 0,
       "max_value": 0
     },
     "savings": 5.4,
     "categories": [
       "Restaurants"
     ],
     "card_type_uuid": "044492f6-0004-4ac4-91d3-a8f661d3b017",
     "name": "TGI Fridays (Voucher)"
   },
   {
     "circle_icon_url": "https://s3.amazonaws.com/raise-content/ibi/CatherinesPlusSizes-Logo.png",
     "brand_uuid": "c4ccc93f-93d9-4639-8b29-30520205e4c3",
     "instant_config": {
       "min_value": 1000,
       "disclaimer": "Redeemable In Store and Online",
       "denominations": [
         2500,
         5000,
         10000,
         25000
       ],
       "gifting_supported": true,
       "increment": 1,
       "max_value": 100000
     },
     "savings": 3,
     "categories": [
       "Women's Apparel"
     ],
     "card_type_uuid": "00bc393b-4c26-4816-a408-176d1308b162",
     "name": "Catherines"
   },
   {
     "circle_icon_url": "https://s3.amazonaws.com/raise-content/ibi/UnderArmour-Logo.png",
     "brand_uuid": "ee4911bd-888c-4185-b5d0-eb0627cd48a1",
     "instant_config": {
       "min_value": 2500,
       "disclaimer": "Redeemable In-Store or Online.",
       "denominations": [
         2500,
         5000,
         7500,
         10000
       ],
       "gifting_supported": true,
       "increment": 1,
       "max_value": 50000
     },
     "savings": 6.1,
     "categories": [
       "Men's Apparel",
       "Sports and Outdoors",
       "Women's Apparel",
       "Weekend Savings"
     ],
     "card_type_uuid": "e6624646-ac86-4345-87ea-dcec6872df5a",
     "name": "Under Armour®"
   },
   {
     "circle_icon_url": "https://s3.amazonaws.com/raise-content/ibi/BooksAMillion-Logo.png",
     "brand_uuid": "1993e875-0a64-4a1a-aab7-4701f8f1e70e",
     "instant_config": {
       "min_value": 0,
       "disclaimer": "Redeemable In Store and Online",
       "denominations": [
         2500
       ],
       "gifting_supported": true,
       "increment": 0,
       "max_value": 0
     },
     "savings": 5,
     "categories": [
       "Books and Magazines"
     ],
     "card_type_uuid": "3ce6d15d-a010-4680-b068-1dca1ce206dc",
     "name": "Books-A-Million"
   },
   {
     "circle_icon_url": "https://s3.amazonaws.com/raise-content/ibi/Airbnb-Logo.png",
     "brand_uuid": "e47cae42-712e-4297-962c-386f04035432",
     "instant_config": {
       "min_value": 0,
       "disclaimer": ""
       "
       Redeemable online.

       Gift card funds can’ t be used to pay
       for the following:

         Reservation of 28 nights or more
       Changes to existing reservations
       The second payment,
       if you choose to pay with the pay less upfront option ""
       ",
       "denominations": [
         5000,
         10000,
         25000,
         50000
       ],
       "gifting_supported": true,
       "increment": 0,
       "max_value": 0
     },
     "savings": 2,
     "categories": [
       "Travel"
     ],
     "card_type_uuid": "2a77b1a6-f684-4d38-ae2a-3f409fd3eac9",
     "name": "Airbnb"
   }

```

This endpoint retrieves all brands.

### HTTP Request

`GET https://api.raise.com/commerce/v1/brands`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
query | empty | Search query to find brands that match keywords.