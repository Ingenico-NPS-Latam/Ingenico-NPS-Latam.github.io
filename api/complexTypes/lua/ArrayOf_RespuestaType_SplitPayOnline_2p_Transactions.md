ArraySplitpayOnline2pTransactions = {}

ArraySplitpayOnline2pTransactions.psp_TransactionId = "100022"
ArraySplitpayOnline2pTransactions.psp_MerchantId = "sdk_test"
ArraySplitpayOnline2pTransactions.psp_MerchTxRef = "ORDER1000-1"
ArraySplitpayOnline2pTransactions.psp_MerchOrderId = "ORDER1000"
ArraySplitpayOnline2pTransactions.psp_MerchAdditionalRef = "ADDITIONAL-REF1234"
ArraySplitpayOnline2pTransactions.psp_Amount = "15050"
ArraySplitpayOnline2pTransactions.psp_NumPayments = "1"
ArraySplitpayOnline2pTransactions.psp_PaymentAmount = "10050"
ArraySplitpayOnline2pTransactions.psp_Product = "14"
ArraySplitpayOnline2pTransactions.psp_CardNumber = "4507990000000010"
ArraySplitpayOnline2pTransactions.psp_CardExpDate = "1906"
ArraySplitpayOnline2pTransactions.psp_AuthorizationCode = "352123"
ArraySplitpayOnline2pTransactions.psp_BatchNro = "1254"
ArraySplitpayOnline2pTransactions.psp_SequenceNumber = "64564321654"
ArraySplitpayOnline2pTransactions.psp_TicketNumber = "1254"
ArraySplitpayOnline2pTransactions.psp_ClTrnId = "365258"
ArraySplitpayOnline2pTransactions.psp_ClExternalMerchant = "96878987"
ArraySplitpayOnline2pTransactions.psp_ClExternalTerminal = "14587986"
ArraySplitpayOnline2pTransactions.psp_ClResponseCod = "155"
ArraySplitpayOnline2pTransactions.psp_ClResponseMsg = "33140"
ArraySplitpayOnline2pTransactions.psp_Plan = "PlanZ"
ArraySplitpayOnline2pTransactions.psp_CreatedAt = "2008-01-12 13:05:35-03:00"

pspAmountAdditionalDetails = {}
pspAmountAdditionalDetails.Tip = "20000"
pspAmountAdditionalDetails.Discount = "11000"

Taxes = {}

Taxes1 = {}
Taxes1.TypeId = "500"
Taxes1.Amount = "10000"
Taxes1.Rate = "2100"
Taxes1.BaseAmount = "10000"

Taxes[#Taxes+1] = Taxes1

Taxes2 = {}
Taxes2.TypeId = "500"
Taxes2.Amount = "10000"
Taxes2.Rate = "2100"
Taxes2.BaseAmount = "10000"

Taxes[#Taxes+1] = Taxes2

pspAmountAdditionalDetails.Taxes = Taxes

ArraySplitpayOnline2pTransactions.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspFraudScreeningResult = {}
pspFraudScreeningResult.ResultCode = "A"
pspFraudScreeningResult.ResultDescription = "ACCEPT"
pspFraudScreeningResult.AdditionalInfo = "Information"

ArraySplitpayOnline2pTransactions.psp_FraudScreeningResult = pspFraudScreeningResult

pspVerificationServicesResult = {}
pspVerificationServicesResult.ResultCodeCardSecurityCode = "M"
pspVerificationServicesResult.ResultCodeBillingAddress = "M"
pspVerificationServicesResult.ResultCodeBillingAddressZipCode = "M"
pspVerificationServicesResult.ResultCodeBillingPersonIDType = "M"
pspVerificationServicesResult.ResultCodeBillingPersonIDNumber = "M"
pspVerificationServicesResult.ResultCodeBillingPersonDateOfBirth = "M"
pspVerificationServicesResult.ResultCodeBillingPersonName = "M"
pspVerificationServicesResult.ResultCodeBillingPersonPhoneNumber1 = "M"
pspVerificationServicesResult.ResultCodeCustomerEmailAddress = "M"

ArraySplitpayOnline2pTransactions.psp_VerificationServicesResult = pspVerificationServicesResult
