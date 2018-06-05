local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


deletepaymentmethod = {}

deletepaymentmethod.psp_Version = "2.2"
deletepaymentmethod.psp_MerchantId = "sdk_test"
deletepaymentmethod.psp_PaymentMethodId = "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE"
deletepaymentmethod.psp_PosDateTime = "2008-01-12 13:05:00"

response = nps.delete_payment_method(deletepaymentmethod)

print(resp.psp_ResponseCod)
