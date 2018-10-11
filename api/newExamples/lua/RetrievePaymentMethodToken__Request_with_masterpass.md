local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


retrievepaymentmethodtoken = {}

retrievepaymentmethodtoken.psp_Version = "2.2"
retrievepaymentmethodtoken.psp_MerchantId = "sdk_test"
retrievepaymentmethodtoken.psp_PaymentMethodToken = "KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM"
retrievepaymentmethodtoken.psp_ClientSession = "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs"

response = nps.retrieve_payment_method_token(retrievepaymentmethodtoken)

print(resp.psp_ResponseCod)
