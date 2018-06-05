local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


retrievecustomer = {}

retrievecustomer.psp_Version = "2.2"
retrievecustomer.psp_MerchantId = "sdk_test"
retrievecustomer.psp_CustomerId = "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b"
retrievecustomer.psp_PosDateTime = "2008-01-12 13:05:00"

response = nps.retrieve_customer(retrievecustomer)

print(resp.psp_ResponseCod)
