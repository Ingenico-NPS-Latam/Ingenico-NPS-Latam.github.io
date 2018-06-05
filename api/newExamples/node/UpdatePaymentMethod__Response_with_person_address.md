response = sdk.updatePaymentMethod(params)

response.psp_ResponseCod
response.psp_ResponseMsg
response.psp_MerchantId

pspPaymentMethod = response.psp_PaymentMethod
pspPaymentMethod.PaymentMethodId
pspPaymentMethod.PaymentMethodTag
pspPaymentMethod.Product

cardOutputDetails = pspPaymentMethod.CardOutputDetails
cardOutputDetails.ExpirationDate
cardOutputDetails.ExpirationYear
cardOutputDetails.ExpirationMonth
cardOutputDetails.HolderName
cardOutputDetails.IIN
cardOutputDetails.Last4
cardOutputDetails.NumberLength
cardOutputDetails.MaskedNumber
cardOutputDetails.MaskedNumberAlternative

pspPaymentMethod.FingerPrint

person = pspPaymentMethod.Person
person.FirstName
person.LastName
person.MiddleName
person.PhoneNumber1
person.PhoneNumber2
person.Gender
person.DateOfBirth
person.Nationality
person.IDNumber
person.IDType


address = pspPaymentMethod.Address
address.Street
address.HouseNumber
address.AdditionalInfo
address.City
address.StateProvince
address.Country
address.ZipCode

pspPaymentMethod.CreatedAt
pspPaymentMethod.UpdatedAt

response.psp_PosDateTime
