# ecomm-apitest-postman
Data driven postman collection runner using newman

This project demonstartes with example how to test an api using POSTMAN. 

The API used for testing is an ecommerce storefront api provided by Shopify https://help.shopify.com/en/api/storefront-api/reference.
More about shopify https://help.shopify.com/en/api/getting-started

Once you have your store setup in shopify, you can use postman collections to test the e2e commerce journey starting from checking price and availability to placing order.

# How to use
Create environment in postman with below variables,
1. access_token - Get storefront access token for your store. https://help.shopify.com/en/api/reference/access/storefrontaccesstoken
2. path - /api/graphql 
3. url - https://domain of the store

The collection has test for availablity and price check request. Add other tests and run using newman.

From the folder where the repository is cloned use to run the collection,

newman run '.\Headless commerce API Test.postman_collection.json' -e .\environmentfile -n 10 -d product_export_postman.csv

# TODO
Add other requests in the journey.

Export results where they can be viewed easily and efficiently.

Use multiple data files.
