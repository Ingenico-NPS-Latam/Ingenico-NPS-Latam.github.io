ArraySplitpayOnline2pTransactions := nps.NewArraySplitpayOnline2pTransactionsStruct()
ArraySplitpayOnline2pTransactions.Psp_TransactionId = "100022"
ArraySplitpayOnline2pTransactions.Psp_MerchantId = "sdk_test"
ArraySplitpayOnline2pTransactions.Psp_MerchTxRef = "ORDER1000-1"
ArraySplitpayOnline2pTransactions.Psp_MerchOrderId = "ORDER1000"
ArraySplitpayOnline2pTransactions.Psp_MerchAdditionalRef = "ADDITIONAL-REF1234"
ArraySplitpayOnline2pTransactions.Psp_Amount = "15050"
ArraySplitpayOnline2pTransactions.Psp_NumPayments = "1"
ArraySplitpayOnline2pTransactions.Psp_PaymentAmount = "10050"
ArraySplitpayOnline2pTransactions.Psp_Product = "14"
ArraySplitpayOnline2pTransactions.Psp_CardNumber = "4507990000000010"
ArraySplitpayOnline2pTransactions.Psp_CardExpDate = "1906"
ArraySplitpayOnline2pTransactions.Psp_AuthorizationCode = "352123"
ArraySplitpayOnline2pTransactions.Psp_BatchNro = "1254"
ArraySplitpayOnline2pTransactions.Psp_SequenceNumber = "64564321654"
ArraySplitpayOnline2pTransactions.Psp_TicketNumber = "1254"
ArraySplitpayOnline2pTransactions.Psp_ClTrnId = "365258"
ArraySplitpayOnline2pTransactions.Psp_ClExternalMerchant = "96878987"
ArraySplitpayOnline2pTransactions.Psp_ClExternalTerminal = "14587986"
ArraySplitpayOnline2pTransactions.Psp_ClResponseCod = "155"
ArraySplitpayOnline2pTransactions.Psp_ClResponseMsg = "33140"
ArraySplitpayOnline2pTransactions.Psp_Plan = "PlanZ"
ArraySplitpayOnline2pTransactions.Psp_CreatedAt = "2008-01-12 13:05:35-03:00"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsRequestStruct()
pspAmountAdditionalDetails.Tip = "20000"
pspAmountAdditionalDetails.Discount = "11000"

Taxes := nps.NewArrayOf_TaxesRequestStruct()
Taxes.Items = make([]*nps.NewTaxesRequestStruct(), 0)

Taxes1 := nps.NewTaxesRequestStruct()
Taxes1.TypeId = "500"
Taxes1.Amount = "10000"
Taxes1.Rate = "2100"
Taxes1.BaseAmount = "10000"
Taxes.Items = append(Taxes.Items, Taxes1)

Taxes2 := nps.NewTaxesRequestStruct()
Taxes2.TypeId = "500"
Taxes2.Amount = "10000"
Taxes2.Rate = "2100"
Taxes2.BaseAmount = "10000"
Taxes.Items = append(Taxes.Items, Taxes2)


ArraySplitpayOnline2pTransactions.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspFraudScreeningResult := nps.NewFraudScreeningResultStruct()
pspFraudScreeningResult.ResultCode = "A"
pspFraudScreeningResult.ResultDescription = "ACCEPT"
pspFraudScreeningResult.AdditionalInfo = "Information"

ArraySplitpayOnline2pTransactions.psp_FraudScreeningResult = pspFraudScreeningResult

pspVerificationServicesResult := nps.NewVerificationServicesResultStruct()
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
