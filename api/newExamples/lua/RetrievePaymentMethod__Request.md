local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


retrievepaymentmethod = {}

retrievepaymentmethod.psp_Version = "2.2"
retrievepaymentmethod.psp_MerchantId = "sdk_test"
retrievepaymentmethod.psp_PaymentMethodId = "jGW24iDaoMBzfKHViL18TmHo9sHBgW4J"
retrievepaymentmethod.psp_PosDateTime = "2008-01-12 13:05:00"

response = nps.retrieve_payment_method(retrievepaymentmethod)

print(resp.psp_ResponseCod)
