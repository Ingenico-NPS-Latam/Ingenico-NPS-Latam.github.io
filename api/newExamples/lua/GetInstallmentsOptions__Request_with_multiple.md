local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


getinstallmentsoptions = {}

getinstallmentsoptions.psp_Version = "2.2"
getinstallmentsoptions.psp_MerchantId = "sdk_test"
getinstallmentsoptions.psp_Amount = "100"
getinstallmentsoptions.psp_Product = "14"
getinstallmentsoptions.psp_Currency = "152"
getinstallmentsoptions.psp_Country = "CHL"
getinstallmentsoptions.psp_NumPayments = "12"
getinstallmentsoptions.psp_PaymentMethodToken = "KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM"
getinstallmentsoptions.psp_ClientSession = "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs"
getinstallmentsoptions.psp_PosDateTime = "2017-04-04 13:35:20"

response = nps.get_installments_options(getinstallmentsoptions)

print(resp.psp_ResponseCod)
