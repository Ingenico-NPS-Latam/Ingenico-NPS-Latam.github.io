
response = nps.create_payment_method_from_payment(createpaymentmethodfrompayment)

print(response.psp_ResponseCod)
print(response.psp_ResponseMsg)
print(response.psp_MerchantId)

local pspPaymentMethod = response.psp_PaymentMethod
print(pspPaymentMethod.PaymentMethodId)
print(pspPaymentMethod.PaymentMethodTag)
print(pspPaymentMethod.Product)

local cardOutputDetails = psp_PaymentMethod.CardOutputDetails
print(cardOutputDetails.ExpirationDate)
print(cardOutputDetails.ExpirationYear)
print(cardOutputDetails.ExpirationMonth)
print(cardOutputDetails.IIN)
print(cardOutputDetails.Last4)
print(cardOutputDetails.NumberLength)
print(cardOutputDetails.MaskedNumber)
print(cardOutputDetails.MaskedNumberAlternative)

print(pspPaymentMethod.FingerPrint)
print(pspPaymentMethod.CreatedAt)
print(pspPaymentMethod.UpdatedAt)

print(response.psp_CustomerId)
print(response.psp_PosDateTime)
