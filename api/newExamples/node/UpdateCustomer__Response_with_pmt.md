response = sdk.updateCustomer(params)

response.psp_ResponseCod
response.psp_ResponseMsg
response.psp_MerchantId
response.psp_CustomerId
response.psp_EmailAddress
response.psp_AlternativeEmailAddress
response.psp_AccountID
response.psp_AccountCreatedAt
response.psp_DefaultPaymentMethodId

var pspPaymentMethods0 = response.psp_PaymentMethods[0]

pspPaymentMethods0.PaymentMethodId
pspPaymentMethods0.Product

cardOutputDetails = pspPaymentMethods0.CardOutputDetails
cardOutputDetails.ExpirationDate
cardOutputDetails.ExpirationYear
cardOutputDetails.ExpirationMonth
cardOutputDetails.HolderName
cardOutputDetails.IIN
cardOutputDetails.Last4
cardOutputDetails.NumberLength
cardOutputDetails.MaskedNumber
cardOutputDetails.MaskedNumberAlternative

pspPaymentMethods0.FingerPrint

person = pspPaymentMethods0.Person
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


address = pspPaymentMethods0.Address
address.Street
address.HouseNumber
address.AdditionalInfo
address.City
address.StateProvince
address.Country
address.ZipCode

pspPaymentMethods0.CreatedAt
pspPaymentMethods0.UpdatedAt


response.psp_PosDateTime
