local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


splitpayonline3p = {}

splitpayonline3p.psp_Version = "2.2"
splitpayonline3p.psp_MerchantId = "sdk_test"
splitpayonline3p.psp_TxSource = "WEB"
splitpayonline3p.psp_MerchOrderId = "ORDER66666"
splitpayonline3p.psp_ReturnURL = "http://localhost/"
splitpayonline3p.psp_FrmLanguage = "es_AR"
splitpayonline3p.psp_Amount = "15050"
splitpayonline3p.psp_Currency = "032"
splitpayonline3p.psp_Country = "ARG"
splitpayonline3p.psp_Product = "14"
splitpayonline3p.psp_PosDateTime = "2019-12-01 12:00:00"

pspVaultReference = {}
pspVaultReference.CustomerId = "K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f"

splitpayonline3p.psp_VaultReference = pspVaultReference

pspTransactions = {}

pspTransactions1 = {}
pspTransactions1.psp_MerchantId = "sdk_test"
pspTransactions1.psp_MerchTxRef = "ORDER66666-3"
pspTransactions1.psp_Product = "14"
pspTransactions1.psp_Amount = "10000"
pspTransactions1.psp_NumPayments = "1"

pspTransactions[#pspTransactions+1] = pspTransactions1

pspTransactions2 = {}
pspTransactions2.psp_MerchantId = "sdk_test"
pspTransactions2.psp_MerchTxRef = "ORDER66666-3"
pspTransactions2.psp_Product = "14"
pspTransactions2.psp_Amount = "5050"
pspTransactions2.psp_NumPayments = "1"

pspTransactions[#pspTransactions+1] = pspTransactions2

splitpayonline3p.psp_Transactions = pspTransactions

response = nps.split_pay_online_3p(splitpayonline3p)

print(resp.psp_ResponseCod)
