local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


createcustomer = {}

createcustomer.psp_Version = "2.2"
createcustomer.psp_MerchantId = "sdk_test"
createcustomer.psp_EmailAddress = "jhon.doe@example.com"
createcustomer.psp_AlternativeEmailAddress = "jdoe@example.com"
createcustomer.psp_AccountID = "jdoe78"
createcustomer.psp_AccountCreatedAt = "2010-10-23"

pspPaymentMethod = {}
pspPaymentMethod.PaymentMethodToken = "KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM"

createcustomer.psp_PaymentMethod = pspPaymentMethod
createcustomer.psp_PosDateTime = "2008-01-12 13:05:00"

response = nps.create_customer(createcustomer)

print(resp.psp_ResponseCod)
