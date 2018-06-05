local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


updatepaymentmethod = {}

updatepaymentmethod.psp_Version = "2.2"
updatepaymentmethod.psp_MerchantId = "sdk_test"
updatepaymentmethod.psp_PaymentMethodId = "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE"
updatepaymentmethod.psp_PaymentMethodTag = "Corporate card"

pspCardInputDetails = {}
pspCardInputDetails.ExpirationDate = "2501"

updatepaymentmethod.psp_CardInputDetails = pspCardInputDetails
updatepaymentmethod.psp_PosDateTime = "2008-01-12 13:05:00"

response = nps.update_payment_method(updatepaymentmethod)

print(resp.psp_ResponseCod)
