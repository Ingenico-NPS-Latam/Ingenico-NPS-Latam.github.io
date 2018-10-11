local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


createpaymentmethodtoken = {}

createpaymentmethodtoken.psp_Version = "2.2"
createpaymentmethodtoken.psp_MerchantId = "sdk_test"

pspWalletInputDetails = {}
pspWalletInputDetails.WalletTypeId = "2"
pspWalletInputDetails.WalletKey = "d084703513e87cd1540a114cd7317e6642eca04e"
pspWalletInputDetails.MerchOrderId = "1efed583-1824-436a-869f-286ebdb22ae9"

createpaymentmethodtoken.psp_WalletInputDetails = pspWalletInputDetails
createpaymentmethodtoken.psp_ClientSession = "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs"

response = nps.create_payment_method_token(createpaymentmethodtoken)

print(resp.psp_ResponseCod)
