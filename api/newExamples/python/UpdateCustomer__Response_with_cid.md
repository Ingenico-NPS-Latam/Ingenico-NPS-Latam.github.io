response = sdk.update_customer(params)

response.get('psp_ResponseCod')
response.get('psp_ResponseMsg')
response.get('psp_MerchantId')
response.get('psp_CustomerId')
response.get('psp_EmailAddress')
response.get('psp_AlternativeEmailAddress')
response.get('psp_AccountID')
response.get('psp_AccountCreatedAt')
response.get('psp_DefaultPaymentMethodId')

pspPaymentMethods0 = response.get('psp_PaymentMethods')[0]

pspPaymentMethods0.get('PaymentMethodId')
pspPaymentMethods0.get('Product')

cardOutputDetails = pspPaymentMethods0.get('CardOutputDetails')
cardOutputDetails.get('ExpirationDate')
cardOutputDetails.get('ExpirationYear')
cardOutputDetails.get('ExpirationMonth')
cardOutputDetails.get('HolderName')
cardOutputDetails.get('IIN')
cardOutputDetails.get('Last4')
cardOutputDetails.get('NumberLength')
cardOutputDetails.get('MaskedNumber')
cardOutputDetails.get('MaskedNumberAlternative')
pspPaymentMethods0.get('FingerPrint')
pspPaymentMethods0.get('CreatedAt')
pspPaymentMethods0.get('UpdatedAt')


response.get('psp_PosDateTime')
