
response = nps.retrieve_payment_method_token(retrievepaymentmethodtoken)

print(response.psp_ResponseCod)
print(response.psp_ResponseMsg)
print(response.psp_MerchantId)
print(response.psp_PaymentMethodToken)
print(response.psp_Product)

local pspWalletOutputDetails = response.psp_WalletOutputDetails

local cardOutputDetails = psp_WalletOutputDetails.CardOutputDetails
print(cardOutputDetails.ExpirationDate)
print(cardOutputDetails.ExpirationYear)
print(cardOutputDetails.ExpirationMonth)
print(cardOutputDetails.HolderName)
print(cardOutputDetails.IIN)
print(cardOutputDetails.Last4)
print(cardOutputDetails.NumberLength)
print(cardOutputDetails.MaskedNumber)
print(cardOutputDetails.MaskedNumberAlternative)


local shippingDetails = psp_WalletOutputDetails.ShippingDetails
print(shippingDetails.Method)

local primaryRecipient = ShippingDetails.PrimaryRecipient
print(primaryRecipient.FirstName)
print(primaryRecipient.PhoneNumber1)


local address = ShippingDetails.Address
print(address.Street)

local houseNumber = Address.HouseNumber

print(address.AdditionalInfo)
print(address.City)
print(address.Country)
print(address.ZipCode)




local pspAddress = response.psp_Address
print(pspAddress.Street)
print(pspAddress.AdditionalInfo)
print(pspAddress.City)
print(pspAddress.Country)
print(pspAddress.ZipCode)

print(response.psp_AlreadyUsed)
print(response.psp_CreatedAt)
print(response.psp_UpdatedAt)
