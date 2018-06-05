local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


createcustomer = {}

createcustomer.psp_Version = "2.2"
createcustomer.psp_MerchantId = "sdk_test"
createcustomer.psp_EmailAddress = "jhon.doe@example.com"
createcustomer.psp_AlternativeEmailAddress = "jdoe@example.com"
createcustomer.psp_AccountID = "jdoe78"
createcustomer.psp_AccountCreatedAt = "2010-10-23"

pspPerson = {}
pspPerson.FirstName = "John"
pspPerson.LastName = "Doe"
pspPerson.MiddleName = "Michael"
pspPerson.PhoneNumber1 = "+1 011 11111111"
pspPerson.PhoneNumber2 = "+1 011 22222222"
pspPerson.DateOfBirth = "1979-01-12"
pspPerson.Gender = "M"
pspPerson.Nationality = "ARG"
pspPerson.IDNumber = "54111111"
pspPerson.IDType = "200"

createcustomer.psp_Person = pspPerson

pspAddress = {}
pspAddress.Street = "Av. Collins"
pspAddress.HouseNumber = "1245"
pspAddress.AdditionalInfo = "2 A"
pspAddress.StateProvince = "Florida"
pspAddress.City = "Miami"
pspAddress.Country = "USA"
pspAddress.ZipCode = "33140"

createcustomer.psp_Address = pspAddress

pspPaymentMethod = {}

CardInputDetails = {}
CardInputDetails.Number = "4507990000000010"
CardInputDetails.ExpirationDate = "2501"
CardInputDetails.SecurityCode = "123"
CardInputDetails.HolderName = "JOHN DOE"

pspPaymentMethod.CardInputDetails = CardInputDetails

Address = {}
Address.Street = "Av. Collins"
Address.HouseNumber = "1245"
Address.AdditionalInfo = "2 A"
Address.StateProvince = "Florida"
Address.City = "Miami"
Address.Country = "USA"
Address.ZipCode = "33140"

pspPaymentMethod.Address = Address

Person = {}
Person.FirstName = "John"
Person.LastName = "Doe"
Person.MiddleName = "Michael"
Person.PhoneNumber1 = "+1 011 11111111"
Person.PhoneNumber2 = "+1 011 22222222"
Person.DateOfBirth = "1979-01-12"
Person.Gender = "M"
Person.Nationality = "ARG"
Person.IDNumber = "54111111"
Person.IDType = "200"

pspPaymentMethod.Person = Person

createcustomer.psp_PaymentMethod = pspPaymentMethod
createcustomer.psp_PosDateTime = "2008-01-12 13:05:00"

response = nps.create_customer(createcustomer)

print(resp.psp_ResponseCod)
