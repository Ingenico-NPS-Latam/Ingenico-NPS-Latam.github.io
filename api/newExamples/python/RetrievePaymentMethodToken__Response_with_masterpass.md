response = sdk.retrieve_payment_method_token(params)

response.get('psp_ResponseCod')
response.get('psp_ResponseMsg')
response.get('psp_MerchantId')
response.get('psp_PaymentMethodToken')
response.get('psp_Product')

pspWalletOutputDetails = response.get('psp_WalletOutputDetails')

cardOutputDetails = pspWalletOutputDetails.get('CardOutputDetails')
cardOutputDetails.get('ExpirationDate')
cardOutputDetails.get('ExpirationYear')
cardOutputDetails.get('ExpirationMonth')
cardOutputDetails.get('HolderName')
cardOutputDetails.get('IIN')
cardOutputDetails.get('Last4')
cardOutputDetails.get('NumberLength')
cardOutputDetails.get('MaskedNumber')
cardOutputDetails.get('MaskedNumberAlternative')

shippingDetails = pspWalletOutputDetails.get('ShippingDetails')
shippingDetails.get('Method')

primaryRecipient = shippingDetails.get('PrimaryRecipient')
primaryRecipient.get('FirstName')
primaryRecipient.get('PhoneNumber1')

address = shippingDetails.get('Address')
address.get('Street')

houseNumber = address.get('HouseNumber')
address.get('AdditionalInfo')
address.get('City')
address.get('Country')
address.get('ZipCode')

pspAddress = response.get('psp_Address')
pspAddress.get('Street')
pspAddress.get('AdditionalInfo')
pspAddress.get('City')
pspAddress.get('Country')
pspAddress.get('ZipCode')
response.get('psp_AlreadyUsed')
response.get('psp_CreatedAt')
response.get('psp_UpdatedAt')
