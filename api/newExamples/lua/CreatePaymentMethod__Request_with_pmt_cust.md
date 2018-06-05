local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


createpaymentmethod = {}

createpaymentmethod.psp_Version = "2.2"
createpaymentmethod.psp_MerchantId = "sdk_test"
createpaymentmethod.psp_CustomerId = "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b"

pspPaymentMethod = {}
pspPaymentMethod.PaymentMethodToken = "HGIYeXKJpQyBvO3pHuZTN9JZiVPnzQaQ"
pspPaymentMethod.PaymentMethodTag = "Corporate card"

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

Address = {}
Address.Street = "Av. Collins"
Address.HouseNumber = "4702"
Address.AdditionalInfo = "2 A"
Address.City = "Buenos Aires"
Address.StateProvince = "CABA"
Address.Country = "ARG"
Address.ZipCode = "1425"

pspPaymentMethod.Address = Address

createpaymentmethod.psp_PaymentMethod = pspPaymentMethod
createpaymentmethod.psp_SetAsCustomerDefault = "1"
createpaymentmethod.psp_PosDateTime = "2008-01-12 13:05:00"

response = nps.create_payment_method(createpaymentmethod)

print(resp.psp_ResponseCod)
