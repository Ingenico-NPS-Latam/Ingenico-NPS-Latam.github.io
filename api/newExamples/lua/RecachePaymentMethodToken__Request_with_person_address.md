local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


recachepaymentmethodtoken = {}

recachepaymentmethodtoken.psp_Version = "2.2"
recachepaymentmethodtoken.psp_MerchantId = "sdk_test"
recachepaymentmethodtoken.psp_PaymentMethodId = "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE"
recachepaymentmethodtoken.psp_CardSecurityCode = "123"

pspPerson = {}
pspPerson.FirstName = "John"
pspPerson.DateOfBirth = "1979-01-12"
pspPerson.LastName = "Doe"
pspPerson.MiddleName = "Michael"
pspPerson.PhoneNumber1 = "+1 011 11111111"
pspPerson.PhoneNumber2 = "+1 011 22222222"
pspPerson.Gender = "M"
pspPerson.Nationality = "ARG"
pspPerson.IDNumber = "54111111"
pspPerson.IDType = "200"

recachepaymentmethodtoken.psp_Person = pspPerson

pspAddress = {}
pspAddress.Street = "Av. Collins"
pspAddress.HouseNumber = "4702"
pspAddress.AdditionalInfo = "2 A"
pspAddress.City = "Buenos Aires"
pspAddress.StateProvince = "CABA"
pspAddress.Country = "ARG"
pspAddress.ZipCode = "1425"

recachepaymentmethodtoken.psp_Address = pspAddress
recachepaymentmethodtoken.psp_ClientSession = "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs"

response = nps.recache_payment_method_token(recachepaymentmethodtoken)

print(resp.psp_ResponseCod)
