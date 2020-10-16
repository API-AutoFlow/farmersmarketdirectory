

# Summary
* Integrate with U.S. Department of Agriculture ("DoA") Farmers market directory API
* Extract data from the API
* Iterate over the data and filter only the name and address

# API AutoFlow Version:
Configuration config.json was created using AutoFlow version __1.0.6__

# Need help?
Is you have questions about this example, feel free to post your question on the community "<a href="https://interactor.com/autoflow/questions" target="_blank">Ask Questions</a>" website.

# API AutoFlow Installation
Visit https://interactor.com/autoflow/download/ to get a free version of API AutoFlow

# DoA integration + Data extraction

## Flow overview
1. HTTP Server
2. Endpoint (Method: GET)
3. Action __string/join__ to join the url with variable zip code
4. Action __communication/http-request__ to make the HTTP API call to DoA
5. Action __json/decode__ to make the JSON easier to use
6. Action __data/set__ to create an empty array for storing the extracted database
7. Action __iteration/for-each__ to iterate over the DoA data which is in array
8. Action __string/join__ to prep the url with each unique farmer's market ID
9. Action __communication/http-request__ API call to get details for each farmer's market
10. Action __json/decode__ to make the JSON easier to use
11. Action __array/insert-at__ to insert the extracted data into the array
12. Action __data/set__ to set the result in the response body


## Simulated Mock data
When build API solution, it is easier to mock the data, which makes it easier to build and test the solution.
