local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


authorize2p = {}

authorize2p.psp_Version = "2.2"
authorize2p.psp_MerchantId = "sdk_test"
authorize2p.psp_TxSource = "WEB"
authorize2p.psp_MerchTxRef = "ORDERX1466Xz-3"
authorize2p.psp_MerchOrderId = "ORDERX1466Xz"
authorize2p.psp_Amount = "1220000"
authorize2p.psp_NumPayments = "1"
authorize2p.psp_Currency = "858"
authorize2p.psp_Country = "URY"
authorize2p.psp_Product = "5"
authorize2p.psp_CardNumber = "5453010000083303"
authorize2p.psp_CardExpDate = "1904"
authorize2p.psp_PosDateTime = "2019-12-01 12:00:00"

pspAmountAdditionalDetails = {}
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes = {}

Taxes1 = {}
Taxes1.TypeId = "601"
Taxes1.Amount = "220000"
Taxes1.Rate = "2200"
Taxes1.BaseAmount = "1000000"

Taxes[#Taxes+1] = Taxes1

pspAmountAdditionalDetails.Taxes = Taxes

authorize2p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspBillingDetails = {}
pspBillingDetails.Invoice = "A00024144"
pspBillingDetails.InvoiceAmount = "1600000"
pspBillingDetails.InvoiceCurrency = "858"

authorize2p.psp_BillingDetails = pspBillingDetails

response = nps.authorize_2p(authorize2p)

print(resp.psp_ResponseCod)
