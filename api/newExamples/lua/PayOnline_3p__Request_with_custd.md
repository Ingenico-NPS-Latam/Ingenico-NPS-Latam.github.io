local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


payonline3p = {}

payonline3p.psp_Version = "2.2"
payonline3p.psp_MerchantId = "sdk_test"
payonline3p.psp_TxSource = "WEB"
payonline3p.psp_MerchTxRef = "ORDER66666-3"
payonline3p.psp_MerchOrderId = "ORDER66666"
payonline3p.psp_ReturnURL = "http://localhost/"
payonline3p.psp_FrmLanguage = "es_AR"
payonline3p.psp_Amount = "15050"
payonline3p.psp_NumPayments = "1"
payonline3p.psp_Currency = "032"
payonline3p.psp_Country = "ARG"
payonline3p.psp_Product = "14"

pspVaultReference = {}
pspVaultReference.CustomerId = "K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f"

payonline3p.psp_VaultReference = pspVaultReference
payonline3p.psp_PosDateTime = "2019-12-01 12:00:00"

response = nps.pay_online_3p(payonline3p)

print(resp.psp_ResponseCod)
