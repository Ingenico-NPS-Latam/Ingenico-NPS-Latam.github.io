response = sdk.updateCustomer(params)

response.psp_ResponseCod
response.psp_ResponseMsg
response.psp_MerchantId
response.psp_CustomerId
response.psp_EmailAddress
response.psp_AlternativeEmailAddress
response.psp_AccountID
response.psp_AccountCreatedAt

pspPerson = response.psp_Person
pspPerson.FirstName
pspPerson.LastName
pspPerson.MiddleName
pspPerson.PhoneNumber1
pspPerson.PhoneNumber2
pspPerson.Gender
pspPerson.DateOfBirth
pspPerson.Nationality
pspPerson.IDNumber
pspPerson.IDType


pspAddress = response.psp_Address
pspAddress.Street
pspAddress.HouseNumber
pspAddress.AdditionalInfo
pspAddress.City
pspAddress.StateProvince
pspAddress.Country
pspAddress.ZipCode

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
pspPaymentMethods0.CreatedAt
pspPaymentMethods0.UpdatedAt


response.psp_PosDateTime
