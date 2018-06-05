local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


recachepaymentmethodtoken = {}

recachepaymentmethodtoken.psp_Version = "2.2"
recachepaymentmethodtoken.psp_MerchantId = "sdk_test"
recachepaymentmethodtoken.psp_PaymentMethodId = "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE"
recachepaymentmethodtoken.psp_CardSecurityCode = "123"
recachepaymentmethodtoken.psp_ClientSession = "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs"

response = nps.recache_payment_method_token(recachepaymentmethodtoken)

print(resp.psp_ResponseCod)
