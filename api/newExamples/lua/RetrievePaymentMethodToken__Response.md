
response = nps.retrieve_payment_method_token(retrievepaymentmethodtoken)

print(response.psp_ResponseCod)
print(response.psp_ResponseMsg)
print(response.psp_MerchantId)
print(response.psp_PaymentMethodToken)
print(response.psp_Product)

local pspCardOutputDetails = response.psp_CardOutputDetails
print(pspCardOutputDetails.ExpirationDate)
print(pspCardOutputDetails.ExpirationYear)
print(pspCardOutputDetails.ExpirationMonth)
print(pspCardOutputDetails.HolderName)
print(pspCardOutputDetails.IIN)
print(pspCardOutputDetails.Last4)
print(pspCardOutputDetails.NumberLength)
print(pspCardOutputDetails.MaskedNumber)
print(pspCardOutputDetails.MaskedNumberAlternative)


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

print(response.psp_AlreadyUsed)
print(response.psp_CreatedAt)
print(response.psp_UpdatedAt)
