response = sdk.pay_online_2p(params)

response.get('psp_ResponseCod')
response.get('psp_ResponseMsg')
response.get('psp_ResponseExtended')
response.get('psp_TransactionId')
response.get('psp_MerchantId')
response.get('psp_MerchTxRef')
response.get('psp_MerchOrderId')
response.get('psp_Amount')
response.get('psp_NumPayments')
response.get('psp_Currency')
response.get('psp_Country')
response.get('psp_Product')
response.get('psp_CardNumber')
response.get('psp_CardExpDate')
response.get('psp_AuthorizationCode')
response.get('psp_SequenceNumber')
response.get('psp_ClExternalMerchant')
response.get('psp_ClResponseCod')
response.get('psp_ClResponseMsg')
response.get('psp_PosDateTime')
response.get('psp_CreatedAt')

pspAmountAdditionalDetails = response.get('psp_AmountAdditionalDetails')
pspAmountAdditionalDetails.get('Tip')
pspAmountAdditionalDetails.get('Discount')

taxes0 = pspAmountAdditionalDetails.get('Taxes')[0]

taxes0.get('TypeId')
taxes0.get('TypeDescription')
taxes0.get('Amount')

rate = taxes0.get('Rate')

baseAmount = taxes0.get('BaseAmount')

appliedAmount = taxes0.get('AppliedAmount')

remarks = taxes0.get('Remarks')



pspFraudScreeningResult = response.get('psp_FraudScreeningResult')
pspFraudScreeningResult.get('ResultCode')
pspFraudScreeningResult.get('ResultDescription')

pspVerificationServicesResult = response.get('psp_VerificationServicesResult')
pspVerificationServicesResult.get('ResultCodeCardSecurityCode')
pspVerificationServicesResult.get('ResultCodeBillingAddress')
pspVerificationServicesResult.get('ResultCodeBillingAddressZipCode')
pspVerificationServicesResult.get('ResultCodeBillingPersonIDType')
pspVerificationServicesResult.get('ResultCodeBillingPersonIDNumber')
pspVerificationServicesResult.get('ResultCodeBillingPersonDateOfBirth')
pspVerificationServicesResult.get('ResultCodeBillingPersonName')
pspVerificationServicesResult.get('ResultCodeBillingPersonPhoneNumber1')
pspVerificationServicesResult.get('ResultCodeCustomerEmailAddress')
