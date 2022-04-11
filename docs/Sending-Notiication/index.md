

# Notify 

To notify us of a successful payment transaction. you are required to send a `POST` request to the endpoint below.

> ` [POST] https://mdw.neolifeafrica.info/banks-sandbox/api/payment`

The payload for the request is described below.


```json
{
    "reference" : 34848484, //Required (Payment reference)
    "customerid" : 44894, // Customer ID (Neolife ID, Phone Number)
    "date" : "2018-01-29 3:30 PM", //Required (Transaction Date)
    "amount" : 90000, // Transaction Amount
    "description": "Transaction Description",
    "hash" : "sha 512 of api_tokenReferenceAmount" //Concantenate api_token, reference and amount and get the sha 512 value of the result.
}

```

## Response 

On either success or failure, you would get a response with a `status` and a `response` key. Example is given below

```json

{
    "status": true,
    "response": "Payment Created Succesfully"
}

```