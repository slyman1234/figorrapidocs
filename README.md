# FIGORR INSURANCE API DOCS 


## INTRODUCTION


     This is a documentation for implementation of this insurance  API into your merchant application.

     With this API you can add the ability for your customers to purchase insurance packages from Figorr.

## AUTHENTICATION AND AUTHORIZATION

    Kindly register with us as a partner using the following url:
    After registration , you have to login to your account to get your API KEY.
    The api key is passed as client Id via when implementing the api on your platform.

## <img width="1277" alt="Screenshot 2023-08-09 at 08 00 40" src="https://github.com/slyman1234/figorrapidocs/assets/103638220/d9d17975-d826-4c30-ba85-c2f7e2623185">

## Below Is The  Documentation For Each Insurance Policy.

## ENDPOINT 1  
## GADGET INSURANCE

## ENDPOINT URL: 
     
    https://figorr-api.onrender.com/figoor/api/gadget/insuregadget

    METHOD: POST

    CONTENT TYPE: "Content-Type": "multipart/form-data".

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
       error: "Cliend id has to start with Bearer with a space before clientid"
    401:   
       error: “Client is unavailable”
    403:   
        error:”Token is invalid”
    404:   
     error:” error applying for insurance”
