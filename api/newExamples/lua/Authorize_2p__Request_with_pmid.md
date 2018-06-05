local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


authorize2p = {}

authorize2p.psp_Version = "2.2"
authorize2p.psp_MerchantId = "sdk_test"
authorize2p.psp_TxSource = "WEB"
authorize2p.psp_MerchTxRef = "ORDERX1466Xz-3"
authorize2p.psp_MerchOrderId = "ORDERX1466Xz"
authorize2p.psp_Amount = "15050"
authorize2p.psp_NumPayments = "1"
authorize2p.psp_Currency = "032"
authorize2p.psp_Country = "ARG"
authorize2p.psp_Product = "14"
authorize2p.psp_PosDateTime = "2019-12-01 12:00:00"

pspVaultReference = {}
pspVaultReference.PaymentMethodId = "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE"

authorize2p.psp_VaultReference = pspVaultReference

response = nps.authorize_2p(authorize2p)

print(resp.psp_ResponseCod)
