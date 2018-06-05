
response = nps.delete_payment_method(deletepaymentmethod)

print(response.psp_ResponseCod)
print(response.psp_ResponseMsg)
print(response.psp_MerchantId)

local pspPaymentMethod = response.psp_PaymentMethod
print(pspPaymentMethod.PaymentMethodId)
print(pspPaymentMethod.PaymentMethodTag)
print(pspPaymentMethod.Product)

local cardOutputDetails = psp_PaymentMethod.CardOutputDetails
print(cardOutputDetails.ExpirationDate)
print(cardOutputDetails.ExpirationYear)
print(cardOutputDetails.ExpirationMonth)
print(cardOutputDetails.HolderName)
print(cardOutputDetails.IIN)
print(cardOutputDetails.Last4)
print(cardOutputDetails.NumberLength)
print(cardOutputDetails.MaskedNumber)
print(cardOutputDetails.MaskedNumberAlternative)

print(pspPaymentMethod.FingerPrint)

local person = psp_PaymentMethod.Person
print(person.FirstName)
print(person.LastName)
print(person.MiddleName)
print(person.PhoneNumber1)
print(person.PhoneNumber2)
print(person.Gender)
print(person.DateOfBirth)
print(person.Nationality)
print(person.IDNumber)
print(person.IDType)


local address = psp_PaymentMethod.Address
print(address.Street)
print(address.HouseNumber)
print(address.AdditionalInfo)
print(address.City)
print(address.StateProvince)
print(address.Country)
print(address.ZipCode)

print(pspPaymentMethod.CreatedAt)
print(pspPaymentMethod.UpdatedAt)

print(response.psp_PosDateTime)
