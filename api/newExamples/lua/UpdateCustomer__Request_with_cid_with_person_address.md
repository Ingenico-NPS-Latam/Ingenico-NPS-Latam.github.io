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

pspPaymentMethod = {}

CardInputDetails = {}
CardInputDetails.Number = "4507990000000010"
CardInputDetails.ExpirationDate = "2501"
CardInputDetails.SecurityCode = "123"
CardInputDetails.HolderName = "JOHN DOE"

pspPaymentMethod.CardInputDetails = CardInputDetails

Person = {}
Person.FirstName = "John"
Person.LastName = "Doe"
Person.MiddleName = "Michael"
Person.PhoneNumber1 = "+1 011 11111111"
Person.PhoneNumber2 = "+1 011 22222222"
Person.Gender = "M"
Person.DateOfBirth = "1979-01-12"
Person.Nationality = "ARG"
Person.IDNumber = "54111111"
Person.IDType = "200"

pspPaymentMethod.Person = Person

Address = {}
Address.Street = "Av. Collins"
Address.HouseNumber = "1245"
Address.AdditionalInfo = "2 A"
Address.City = "Miami"
Address.StateProvince = "Florida"
Address.Country = "USA"
Address.ZipCode = "33140"

pspPaymentMethod.Address = Address

updatecustomer.psp_PaymentMethod = pspPaymentMethod
updatecustomer.psp_PosDateTime = "2008-01-12 13:05:00"

response = nps.update_customer(updatecustomer)

print(resp.psp_ResponseCod)
