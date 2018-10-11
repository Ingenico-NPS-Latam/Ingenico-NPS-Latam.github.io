response = sdk.createPaymentMethodToken(params)

response.psp_ResponseCod
response.psp_ResponseMsg
response.psp_MerchantId
response.psp_PaymentMethodToken
response.psp_Product

pspWalletOutputDetails = response.psp_WalletOutputDetails

cardOutputDetails = pspWalletOutputDetails.CardOutputDetails
cardOutputDetails.ExpirationDate
cardOutputDetails.ExpirationYear
cardOutputDetails.ExpirationMonth
cardOutputDetails.HolderName
cardOutputDetails.IIN
cardOutputDetails.Last4
cardOutputDetails.NumberLength
cardOutputDetails.MaskedNumber
cardOutputDetails.MaskedNumberAlternative


shippingDetails = pspWalletOutputDetails.ShippingDetails
shippingDetails.Method

primaryRecipient = shippingDetails.PrimaryRecipient
primaryRecipient.FirstName
primaryRecipient.PhoneNumber1


address = shippingDetails.Address
address.Street

houseNumber = address.HouseNumber

address.AdditionalInfo
address.City
address.Country
address.ZipCode




pspAddress = response.psp_Address
pspAddress.Street
pspAddress.AdditionalInfo
pspAddress.City
pspAddress.Country
pspAddress.ZipCode

response.psp_AlreadyUsed
response.psp_CreatedAt
response.psp_UpdatedAt
