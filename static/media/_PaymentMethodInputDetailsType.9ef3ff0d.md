ComplexElement paymentMethodInputDetails = response.getComplexElement("PaymentMethodInputDetails");


local pspPaymentMethodInputDetails = paymentMethodInputDetails.psp_PaymentMethodInputDetails
print(pspPaymentMethodInputDetails.PaymentMethodToken)
print(pspPaymentMethodInputDetails.PaymentMethodTag)

local cardInputDetails = psp_PaymentMethodInputDetails.CardInputDetails
print(cardInputDetails.Number)
print(cardInputDetails.ExpirationDate)
print(cardInputDetails.SecurityCode)
print(cardInputDetails.HolderName)


local person = psp_PaymentMethodInputDetails.Person
print(person.DateOfBirth)
print(person.FirstName)
print(person.Gender)
print(person.IDNumber)
print(person.IDType)
print(person.LastName)
print(person.MiddleName)
print(person.Nationality)
print(person.PhoneNumber1)
print(person.PhoneNumber2)


local address = psp_PaymentMethodInputDetails.Address
print(address.AdditionalInfo)
print(address.City)
print(address.Country)
print(address.HouseNumber)
print(address.StateProvince)
print(address.Street)
print(address.ZipCode)


