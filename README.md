# FIGORR INSURANCE API DOCS 


## INTRODUCTION


     This is a documentation for implementation of this insurance  API into your merchant application.

     With this API you can add the ability for your customers to purchase insurance packages from Figorr.

## AUTHENTICATION AND AUTHORIZATION

    Kindly register with us as a partner using the following url:
    After registration , you have to login to your account to get your API KEY.
    The api key is passed as client Id via when implementing the api on your platform.

    you have the LIve api Key and the Sandboxapi Key.
    
    The live api key is used for Production while the SandBox Api Key is used for Developement


## AUTH ERROR RESPONSE 

    403 0K:
       error: api key does not match
    401:   
       error: "Api Key is required"
  


## Below Is The  Documentation For Each Insurance Policy.

## ENDPOINT 1  
## FETCH ALL INSURANCE POLICY


The folling endpoint is use to fetch all available insurance policies

## ENDPOINT URL: 
     
    https://figorr-api.onrender.com/figoor/api/viewproduct/v1

    METHOD: GET

       headers: {
          "Content-Type": "application/json",
          "api-key": 'api-key',
        },

## REQUEST:

    {
    fullname: { type: String, required: true },
    dob: { type: String, required: true },
    email: { type: String, required: true },
    phone: { type: String, required: true },
    identitypicture: { type: file, required: true },
    gadgetimeinumber: { type: String, required: true },
    pictureofdevice: { type: file, required: true },
    receiptofdevice: { type: file, required: true },
    amount: { type: String, required: true },
    }

## RESPONSE:

    200 0K:
       SUCCESSFUL
    402:   
       error: "No Available product"
    404:   
       error: “Error Fetching Products”

     

## ENDPOINT 2 
## INSURANCE PREMIUM CALCULATION

## ENDPOINT URL: 
     
    https://figorr-api.onrender.com/figoor/api/products/calculateproduct

    METHOD: POST

     headers: {
          "Content-Type": "application/json",
          "api-key": 'api-key',
        },


## REQUEST:

    {
    id: { type: String, required: true }, // INSURANCE POLICY ID
    amount: { type: String, required: true }, // INSURER COST AMOUNT
    }

## RESPONSE:

    200 0K:
       SUCCESSFUL
    402:   
       error: "Error no available products"
    406:   
       error: “Error fetching products”
  




## ENDPOINT 3 
##  INSURANCE  APPLICATION

## ENDPOINT URL: 
     
    https://figorr-api.onrender.com/figoor/api/v1/insurance

    METHOD: POST

         headers: {
         "Content-Type": "multipart/form-data".
          "api-key": 'api-key',
        },



## REQUEST:

    {
    policyid: { type: String, required: false },
    policyname:{ type: String, required: false },
    fullname: { type: String, required: false },
    dob: { type: String, required: false },
    email: { type: String, required: false },
    phone: { type: String, required: false },
    gadgetimeinumber: { type: String, required: false },
    identitypicture: { type: FILE, required: false },
    carparticulars: { type: FILE, required: false },
    driverlicense: { type: FILE, required: false },
    carvalue: { type: String, required: false },
    chasisno: { type: String, required: false },
    pictureofvehicle: { FILE: String, required: false },
    pictureofdevice: { FILE: String, required: false },
    receiptofdevice: { FILE: String, required: false },
    amount: { type: String, required: false },
    claimexpected: { type: String, required: false },
    }

## RESPONSE:

    200 0K:
       SUCCESSFUL

    404:   
     error:” error applying for insurance”





