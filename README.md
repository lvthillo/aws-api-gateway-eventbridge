# AWS API Gateway - EventBridge Integration

![blog drawio](https://github.com/lvthillo/aws-api-gateway-eventbridge/assets/14105387/2622dd0a-183e-48d3-b3f7-a7a3cf7c0e96)

Example request:
```
curl --location --request POST https://xyz.execute-api.eu-west-1.amazonaws.com/prod/CarDetails --header 'Content-Type: application/json' \
--data-raw '
{
    "items":[
        {
            "CarData":"{\"data\":\"Audi A4 is created\"}",
            "BrandType":"audi",
            "Source": "car_data"
        }
    ]
}'
```

* If `BrandType` contains `audi`, it is sent to the audi SQS queue
* If `BrandType` contains `bmw`, it is sent to the bmw SQS queue
