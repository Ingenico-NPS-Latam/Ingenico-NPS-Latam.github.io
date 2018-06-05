ComplexElement paymentMethodOutputDetails = response.getComplexElement("PaymentMethodOutputDetails");


local pspPaymentMethodOutputDetails = paymentMethodOutputDetails.psp_PaymentMethodOutputDetails
print(pspPaymentMethodOutputDetails.PaymentMethodId)
print(pspPaymentMethodOutputDetails.PaymentMethodTag)
print(pspPaymentMethodOutputDetails.Product)

local cardOutputDetails = psp_PaymentMethodOutputDetails.CardOutputDetails
print(cardOutputDetails.ExpirationDate)
print(cardOutputDetails.ExpirationYear)
print(cardOutputDetails.ExpirationMonth)
print(cardOutputDetails.HolderName)
print(cardOutputDetails.IIN)
print(cardOutputDetails.Last4)
print(cardOutputDetails.NumberLength)
print(cardOutputDetails.MaskedNumber)
print(cardOutputDetails.MaskedNumberAlternative)

print(pspPaymentMethodOutputDetails.FingerPrint)

local person = psp_PaymentMethodOutputDetails.Person
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


local address = psp_PaymentMethodOutputDetails.Address
print(address.AdditionalInfo)
print(address.City)
print(address.Country)
print(address.HouseNumber)
print(address.StateProvince)
print(address.Street)
print(address.ZipCode)

print(pspPaymentMethodOutputDetails.CreatedAt)
print(pspPaymentMethodOutputDetails.UpdatedAt)

