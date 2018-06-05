local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


createpaymentmethodtoken = {}

createpaymentmethodtoken.psp_Version = "2.2"
createpaymentmethodtoken.psp_MerchantId = "sdk_test"

pspCardInputDetails = {}
pspCardInputDetails.Number = "4507990000000010"
pspCardInputDetails.ExpirationDate = "2501"
pspCardInputDetails.SecurityCode = "123"
pspCardInputDetails.HolderName = "JOHN DOE"

createpaymentmethodtoken.psp_CardInputDetails = pspCardInputDetails

pspPerson = {}
pspPerson.FirstName = "John"
pspPerson.LastName = "Doe"
pspPerson.MiddleName = "Michael"
pspPerson.DateOfBirth = "1979-01-12"
pspPerson.PhoneNumber1 = "+1 011 11111111"
pspPerson.PhoneNumber2 = "+1 011 22222222"
pspPerson.Gender = "M"
pspPerson.Nationality = "ARG"
pspPerson.IDNumber = "54111111"
pspPerson.IDType = "200"

createpaymentmethodtoken.psp_Person = pspPerson

pspAddress = {}
pspAddress.Street = "Av. Collins"
pspAddress.HouseNumber = "4702"
pspAddress.AdditionalInfo = "2 A"
pspAddress.City = "Buenos Aires"
pspAddress.StateProvince = "CABA"
pspAddress.Country = "ARG"
pspAddress.ZipCode = "1425"

createpaymentmethodtoken.psp_Address = pspAddress
createpaymentmethodtoken.psp_ClientSession = "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs"

response = nps.create_payment_method_token(createpaymentmethodtoken)

print(resp.psp_ResponseCod)
