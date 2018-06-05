
response = nps.update_customer(updatecustomer)

print(response.psp_ResponseCod)
print(response.psp_ResponseMsg)
print(response.psp_MerchantId)
print(response.psp_CustomerId)
print(response.psp_EmailAddress)
print(response.psp_AlternativeEmailAddress)
print(response.psp_AccountID)
print(response.psp_AccountCreatedAt)

local pspPerson = response.psp_Person
print(pspPerson.FirstName)
print(pspPerson.LastName)
print(pspPerson.MiddleName)
print(pspPerson.PhoneNumber1)
print(pspPerson.PhoneNumber2)
print(pspPerson.Gender)
print(pspPerson.DateOfBirth)
print(pspPerson.Nationality)
print(pspPerson.IDNumber)
print(pspPerson.IDType)


local pspAddress = response.psp_Address
print(pspAddress.Street)
print(pspAddress.HouseNumber)
print(pspAddress.AdditionalInfo)
print(pspAddress.City)
print(pspAddress.StateProvince)
print(pspAddress.Country)
print(pspAddress.ZipCode)

print(response.psp_DefaultPaymentMethodId)

local pspPaymentMethods = response.Psp_PaymentMethods

localpspPaymentMethods1 := pspPaymentMethods[1]
print(pspPaymentMethods1.PaymentMethodId)
print(pspPaymentMethods1.Product)

local cardOutputDetails = pspPaymentMethods1.CardOutputDetails
print(cardOutputDetails.ExpirationDate)
print(cardOutputDetails.ExpirationYear)
print(cardOutputDetails.ExpirationMonth)
print(cardOutputDetails.HolderName)
print(cardOutputDetails.IIN)
print(cardOutputDetails.Last4)
print(cardOutputDetails.NumberLength)
print(cardOutputDetails.MaskedNumber)
print(cardOutputDetails.MaskedNumberAlternative)

print(pspPaymentMethods1.FingerPrint)
print(pspPaymentMethods1.CreatedAt)
print(pspPaymentMethods1.UpdatedAt)


print(response.psp_PosDateTime)
