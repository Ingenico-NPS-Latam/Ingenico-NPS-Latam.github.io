local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


createpaymentmethodtoken = {}

createpaymentmethodtoken.psp_Version = "2.2"
createpaymentmethodtoken.psp_MerchantId = "sdk_test"

pspCardInputDetails = {}
pspCardInputDetails.Number = "4507990000000010"
pspCardInputDetails.ExpirationDate = "2501"
pspCardInputDetails.SecurityCode = "123"
pspCardInputDetails.HolderName = "JOHN DOE"

createpaymentmethodtoken.psp_CardInputDetails = pspCardInputDetails
createpaymentmethodtoken.psp_ClientSession = "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs"

response = nps.create_payment_method_token(createpaymentmethodtoken)

print(resp.psp_ResponseCod)
