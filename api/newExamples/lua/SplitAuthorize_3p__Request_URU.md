local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


splitauthorize3p = {}

splitauthorize3p.psp_Version = "2.2"
splitauthorize3p.psp_MerchantId = "sdk_test"
splitauthorize3p.psp_TxSource = "WEB"
splitauthorize3p.psp_MerchOrderId = "ORDER66666"
splitauthorize3p.psp_ReturnURL = "http://localhost/"
splitauthorize3p.psp_FrmLanguage = "es_AR"
splitauthorize3p.psp_Amount = "2440000"
splitauthorize3p.psp_Currency = "858"
splitauthorize3p.psp_Country = "URY"
splitauthorize3p.psp_Product = "5"
splitauthorize3p.psp_PosDateTime = "2019-12-01 12:00:00"

pspBillingDetails = {}
pspBillingDetails.Invoice = "A00024144"
pspBillingDetails.InvoiceAmount = "1600000"
pspBillingDetails.InvoiceCurrency = "858"

splitauthorize3p.psp_BillingDetails = pspBillingDetails

pspTransactions = {}

pspTransactions1 = {}
pspTransactions1.psp_MerchantId = "sdk_test"
pspTransactions1.psp_MerchTxRef = "ORDER66666-3"
pspTransactions1.psp_Product = "5"
pspTransactions1.psp_Amount = "1220000"
pspTransactions1.psp_NumPayments = "1"

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

pspTransactions1.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspTransactions[#pspTransactions+1] = pspTransactions1

pspTransactions2 = {}
pspTransactions2.psp_MerchantId = "sdk_test"
pspTransactions2.psp_MerchTxRef = "ORDER66666-3"
pspTransactions2.psp_Product = "5"
pspTransactions2.psp_Amount = "1220000"
pspTransactions2.psp_NumPayments = "1"

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

pspTransactions2.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspTransactions[#pspTransactions+1] = pspTransactions2

splitauthorize3p.psp_Transactions = pspTransactions

response = nps.split_authorize_3p(splitauthorize3p)

print(resp.psp_ResponseCod)
