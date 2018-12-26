
response = nps.authorize_2p(authorize2p)

print(response.psp_ResponseCod)
print(response.psp_ResponseMsg)
print(response.psp_ResponseExtended)
print(response.psp_TransactionId)
print(response.psp_MerchantId)
print(response.psp_MerchTxRef)
print(response.psp_MerchOrderId)
print(response.psp_Amount)
print(response.psp_NumPayments)
print(response.psp_Currency)
print(response.psp_Country)
print(response.psp_Product)
print(response.psp_CardExpDate)
print(response.psp_AuthorizationCode)
print(response.psp_BatchNro)
print(response.psp_TicketNumber)
print(response.psp_ClExternalMerchant)
print(response.psp_ClExternalTerminal)
print(response.psp_ClResponseCod)
print(response.psp_ClResponseMsg)
print(response.psp_PosDateTime)
print(response.psp_CreatedAt)

local pspFraudScreeningResult = response.psp_FraudScreeningResult
print(pspFraudScreeningResult.ResultCode)
print(pspFraudScreeningResult.ResultDescription)


local pspVerificationServicesResult = response.psp_VerificationServicesResult
print(pspVerificationServicesResult.ResultCodeCardSecurityCode)
print(pspVerificationServicesResult.ResultCodeBillingAddress)
print(pspVerificationServicesResult.ResultCodeBillingAddressZipCode)
print(pspVerificationServicesResult.ResultCodeBillingPersonIDType)
print(pspVerificationServicesResult.ResultCodeBillingPersonIDNumber)
print(pspVerificationServicesResult.ResultCodeBillingPersonDateOfBirth)
print(pspVerificationServicesResult.ResultCodeBillingPersonName)
print(pspVerificationServicesResult.ResultCodeBillingPersonPhoneNumber1)
print(pspVerificationServicesResult.ResultCodeCustomerEmailAddress)
