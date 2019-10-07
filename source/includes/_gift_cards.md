# Cards

## Generate a Card

```ruby
require 'raise_api'

api = Raise::APIClient.authorize!('user')
api.cards.generate('brand_name', denomination)
```

```python
import raise_api

api = raise_api.authorize('user')
api.cards.generate('brand_name', denomination)
```

```shell
curl -X POST "https://api.raise.com/commerce/v1/cards"
  -H "Authorization: user Content-type: application/json"
  -d {
 "user_email": "conlin.mcmanus@raise.com",
 "user_uid": "2a77b1a6-f684-4d38-ae2a-3f409", // This should be a uuid or id passed by the client that can be used to identify the user that made the purchase of this specific gift card during the reconciliation process.
 "instant_config_uuid": "e47cae42-712e-4297-962c-386f04035345",
 "denomination": "8795", // This is the amount to be generated for the gift card. (number should be in cents)
}

```

```javascript
const api = require('raise_api');

let api_client = api.authorize('user');
let card = api.cards.generate();
```

> The above command returns JSON structured like this:

```json
{
 "card_number": "12341234",
 "csc": "12341234",
 "upc": "ABC",
 "barcode": {
   "kind": "code128",
   "value": "2112321122321311231122321311233131212331112",
 },
 "balance": 8795,// balance is in cents
 "card_uuid": "d0f90f9d-acec-4374-bfad-4c02b8e3feef",
}



```

This endpoint generates a card for a given brand, identified by `brand_id`.

### HTTP Request

`POST https://api.raise.com/commerce/v1/cards`