
response = nps.create_payment_method_token(createpaymentmethodtoken)

print(response.psp_ResponseCod)
print(response.psp_ResponseMsg)
print(response.psp_MerchantId)
print(response.psp_PaymentMethodToken)
print(response.psp_Product)

local pspCardOutputDetails = response.psp_CardOutputDetails
print(pspCardOutputDetails.ExpirationDate)
print(pspCardOutputDetails.ExpirationYear)
print(pspCardOutputDetails.ExpirationMonth)
print(pspCardOutputDetails.HolderName)
print(pspCardOutputDetails.IIN)
print(pspCardOutputDetails.Last4)
print(pspCardOutputDetails.NumberLength)
print(pspCardOutputDetails.MaskedNumber)
print(pspCardOutputDetails.MaskedNumberAlternative)

print(response.psp_AlreadyUsed)
print(response.psp_CreatedAt)
print(response.psp_UpdatedAt)
