local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


deletecustomer = {}

deletecustomer.psp_Version = "2.2"
deletecustomer.psp_MerchantId = "sdk_test"
deletecustomer.psp_CustomerId = "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b"
deletecustomer.psp_PosDateTime = "2008-01-12 13:05:00"

response = nps.delete_customer(deletecustomer)

print(resp.psp_ResponseCod)
