local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


payonline2p = {}

payonline2p.psp_Version = "2.2"
payonline2p.psp_MerchantId = "sdk_test"
payonline2p.psp_TxSource = "WEB"
payonline2p.psp_MerchTxRef = "ORDERX1466Xz-3"
payonline2p.psp_MerchOrderId = "ORDERX1466Xz"
payonline2p.psp_Amount = "1220000"
payonline2p.psp_NumPayments = "1"
payonline2p.psp_Currency = "858"
payonline2p.psp_Country = "URY"
payonline2p.psp_Product = "5"
payonline2p.psp_CardNumber = "5453010000083303"
payonline2p.psp_CardExpDate = "1904"
payonline2p.psp_PosDateTime = "2019-12-01 12:00:00"

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

payonline2p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspBillingDetails = {}
pspBillingDetails.Invoice = "A00024144"
pspBillingDetails.InvoiceAmount = "1600000"
pspBillingDetails.InvoiceCurrency = "858"

payonline2p.psp_BillingDetails = pspBillingDetails

response = nps.pay_online_2p(payonline2p)

print(resp.psp_ResponseCod)
