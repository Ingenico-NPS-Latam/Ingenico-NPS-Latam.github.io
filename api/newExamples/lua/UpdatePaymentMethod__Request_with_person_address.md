local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


updatepaymentmethod = {}

updatepaymentmethod.psp_Version = "2.2"
updatepaymentmethod.psp_MerchantId = "sdk_test"
updatepaymentmethod.psp_PaymentMethodId = "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE"
updatepaymentmethod.psp_PaymentMethodTag = "Corporate card"

pspCardInputDetails = {}
pspCardInputDetails.ExpirationDate = "2501"
pspCardInputDetails.HolderName = "JOHN DOE"

updatepaymentmethod.psp_CardInputDetails = pspCardInputDetails

pspPerson = {}
pspPerson.FirstName = "John"
pspPerson.LastName = "Doe"
pspPerson.MiddleName = "Michael"
pspPerson.PhoneNumber1 = "+1 011 11111111"
pspPerson.PhoneNumber2 = "+1 011 22222222"
pspPerson.DateOfBirth = "1979-01-12"
pspPerson.Nationality = "ARG"
pspPerson.Gender = "M"
pspPerson.IDNumber = "54111111"
pspPerson.IDType = "200"

updatepaymentmethod.psp_Person = pspPerson

pspAddress = {}
pspAddress.Street = "Av. Collins"
pspAddress.HouseNumber = "4702"
pspAddress.AdditionalInfo = "2 A"
pspAddress.StateProvince = "CABA"
pspAddress.City = "Buenos Aires"
pspAddress.Country = "ARG"
pspAddress.ZipCode = "1425"

updatepaymentmethod.psp_Address = pspAddress
updatepaymentmethod.psp_PosDateTime = "2008-01-12 13:05:00"

response = nps.update_payment_method(updatepaymentmethod)

print(resp.psp_ResponseCod)
