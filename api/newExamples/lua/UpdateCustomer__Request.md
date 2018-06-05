local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


updatecustomer = {}

updatecustomer.psp_Version = "2.2"
updatecustomer.psp_MerchantId = "sdk_test"
updatecustomer.psp_CustomerId = "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b"
updatecustomer.psp_EmailAddress = "jhon.doe@example.com"
updatecustomer.psp_AlternativeEmailAddress = "jdoe@example.com"
updatecustomer.psp_AccountCreatedAt = "2010-10-23"
updatecustomer.psp_AccountID = "jdoe78"

pspPerson = {}
pspPerson.FirstName = "John"
pspPerson.LastName = "Doe"
pspPerson.MiddleName = "Michael"
pspPerson.PhoneNumber1 = "+1 011 11111111"
pspPerson.PhoneNumber2 = "+1 011 22222222"
pspPerson.Gender = "M"
pspPerson.DateOfBirth = "1979-01-12"
pspPerson.Nationality = "ARG"
pspPerson.IDNumber = "54111111"
pspPerson.IDType = "200"

updatecustomer.psp_Person = pspPerson

pspAddress = {}
pspAddress.Street = "Av. Collins"
pspAddress.HouseNumber = "1245"
pspAddress.AdditionalInfo = "2 A"
pspAddress.City = "Miami"
pspAddress.StateProvince = "Florida"
pspAddress.Country = "USA"
pspAddress.ZipCode = "33140"

updatecustomer.psp_Address = pspAddress
updatecustomer.psp_PosDateTime = "2008-01-12 13:05:00"

response = nps.update_customer(updatecustomer)

print(resp.psp_ResponseCod)
