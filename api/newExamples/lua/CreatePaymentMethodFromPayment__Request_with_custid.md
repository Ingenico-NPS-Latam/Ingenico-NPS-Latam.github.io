local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


createpaymentmethodfrompayment = {}

createpaymentmethodfrompayment.psp_Version = "2.2"
createpaymentmethodfrompayment.psp_MerchantId = "sdk_test"
createpaymentmethodfrompayment.psp_TransactionId = "65340022"
createpaymentmethodfrompayment.psp_PaymentMethodTag = "Corporate card"
createpaymentmethodfrompayment.psp_CustomerId = "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b"
createpaymentmethodfrompayment.psp_SetAsCustomerDefault = "1"
createpaymentmethodfrompayment.psp_PosDateTime = "2008-01-12 13:05:00"

response = nps.create_payment_method_from_payment(createpaymentmethodfrompayment)

print(resp.psp_ResponseCod)
