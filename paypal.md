# Subscription integration
-  Create an app
- get the `client_id` and `secret` of the app
- send this curl to get an access token
```shell
curl -v https://api.sandbox.paypal.com/v1/oauth2/token \
  -H "Accept: application/json" \
  -u "CLIENT_ID:SECRET" \
  -d "grant_type=client_credentials" | jq -r .access_token
```
- send this curl to create product
```shell

curl -v -X POST https://api-m.sandbox.paypal.com/v1/catalogs/products
  -H "Content-Type: application/json"   -H "Authorization: Bearer ACCESS-TOKEN"   -H "PayPal-Request-Id: REQUEST-ID"   -d '{
  "name": "Video Streaming Service",
  "description": "A video streaming service",
  "type": "SERVICE",
  "category": "SOFTWARE",
  "image_url": "https://example.com/streaming.jpg",
  "home_url": "https://example.com/home"
}'
```
## What i've learned the hard way



