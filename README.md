# products-be-lambda

## Setting up configuration and deploying the app

- git clone
- change region in serverless.yml
- run `sls deploy` to deploy the app to aws

You can login to aws console and and can verify the lambda function being created and running.

You can also goto the URL provided by the AWS Gateway API to fetch list of products.

### Note
- One for fetching the list of products
- Another for fetching the product by id

### Endpoints:
  GET - https://mrq9lnbtt5.execute-api.ap-south-1.amazonaws.com/products
  GET - https://mrq9lnbtt5.execute-api.ap-south-1.amazonaws.com/products/{id}

## Additional

- Async/await is used in lambda functions
- ES6 modules are used for Product Service implementation
- Lambda handlers (getProductsList, getProductsById) code is written not in 1 single module (file) and separated in codebase
- Main error scenarios are handled by API ("Product not found" error)