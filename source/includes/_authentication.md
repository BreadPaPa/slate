# Authentication

> To authorize, use this code:

```ruby
require 'raise_api'

api = Raise::APIClient.authorize!('user')
```

```python
import raise_api

api = raise_api.authorize('user')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: user"
```

```javascript
const raise_api = require('raise_api');

let api = raise_api.authorize('user');
```

> Make sure to replace `user` with your API key.

Raise uses API keys to allow access to the API. You can register a new API key at our [developer portal](http://example.com/developers).

Raise API expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: user`

<aside class="notice">
You must replace <code>user</code> with your personal API key.
</aside>