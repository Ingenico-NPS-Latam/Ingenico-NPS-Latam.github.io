ComplexElement paymentMethodsOutputDetails = response.getComplexElement("PaymentMethodsOutputDetails");


local pspPaymentMethodsOutputDetails = paymentMethodsOutputDetails.psp_PaymentMethodsOutputDetails
print(pspPaymentMethodsOutputDetails.PaymentMethodId)
print(pspPaymentMethodsOutputDetails.PaymentMethodTag)
print(pspPaymentMethodsOutputDetails.Product)

local cardOutputDetails = psp_PaymentMethodsOutputDetails.CardOutputDetails
print(cardOutputDetails.ExpirationDate)
print(cardOutputDetails.ExpirationYear)
print(cardOutputDetails.ExpirationMonth)
print(cardOutputDetails.HolderName)
print(cardOutputDetails.IIN)
print(cardOutputDetails.Last4)
print(cardOutputDetails.MaskedNumber)
print(cardOutputDetails.MaskedNumberAlternative)

print(pspPaymentMethodsOutputDetails.FingerPrint)

local person = psp_PaymentMethodsOutputDetails.Person
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


local address = psp_PaymentMethodsOutputDetails.Address
print(address.AdditionalInfo)
print(address.City)
print(address.Country)
print(address.HouseNumber)
print(address.StateProvince)
print(address.Street)
print(address.ZipCode)

print(pspPaymentMethodsOutputDetails.CreatedAt)
print(pspPaymentMethodsOutputDetails.UpdatedAt)

