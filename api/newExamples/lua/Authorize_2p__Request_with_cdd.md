local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


authorize2p = {}

authorize2p.psp_Version = "2.2"
authorize2p.psp_MerchantId = "sdk_test"
authorize2p.psp_TxSource = "WEB"
authorize2p.psp_MerchTxRef = "ORDERX1466Xz-3"
authorize2p.psp_MerchOrderId = "ORDERX1466Xz"
authorize2p.psp_Amount = "15050"
authorize2p.psp_NumPayments = "1"
authorize2p.psp_Currency = "032"
authorize2p.psp_Country = "ARG"
authorize2p.psp_Product = "14"
authorize2p.psp_CardNumber = "4507990000000010"
authorize2p.psp_CardExpDate = "1912"
authorize2p.psp_PosDateTime = "2019-12-01 12:00:00"

pspBillingDetails = {}
pspBillingDetails.Invoice = "54877555"
pspBillingDetails.InvoiceDate = "2017-10-23"
pspBillingDetails.InvoiceAmount = "15050"
pspBillingDetails.InvoiceCurrency = "032"

Person = {}
Person.DateOfBirth = "1979-01-12"
Person.FirstName = "John"
Person.Gender = "M"
Person.IDNumber = "54111111"
Person.IDType = "200"
Person.LastName = "Doe"
Person.MiddleName = "Michael"
Person.Nationality = "ARG"
Person.PhoneNumber1 = "+1 011 11111111"
Person.PhoneNumber2 = "+1 011 22222222"

pspBillingDetails.Person = Person

Address = {}
Address.AdditionalInfo = "2 A"
Address.City = "Miami"
Address.Country = "USA"
Address.HouseNumber = "1245"
Address.StateProvince = "Florida"
Address.Street = "Av. Collins"
Address.ZipCode = "33140"

pspBillingDetails.Address = Address

authorize2p.psp_BillingDetails = pspBillingDetails

pspShippingDetails = {}
pspShippingDetails.TrackingNumber = "154DDD54DWW11"
pspShippingDetails.Method = "10"
pspShippingDetails.Carrier = "200"
pspShippingDetails.DeliveryDate = "2014-11-20"
pspShippingDetails.FreightAmount = "15000"
pspShippingDetails.GiftMessage = "Happy Birthday!"
pspShippingDetails.GiftWrapping = "1"

PrimaryRecipient = {}
PrimaryRecipient.DateOfBirth = "1979-01-12"
PrimaryRecipient.FirstName = "John"
PrimaryRecipient.Gender = "M"
PrimaryRecipient.IDNumber = "54111111"
PrimaryRecipient.IDType = "200"
PrimaryRecipient.LastName = "Doe"
PrimaryRecipient.MiddleName = "Michael"
PrimaryRecipient.Nationality = "ARG"
PrimaryRecipient.PhoneNumber1 = "+1 011 11111111"
PrimaryRecipient.PhoneNumber2 = "+1 011 22222222"

pspShippingDetails.PrimaryRecipient = PrimaryRecipient

SecondaryRecipient = {}
SecondaryRecipient.DateOfBirth = "1979-01-12"
SecondaryRecipient.FirstName = "John"
SecondaryRecipient.Gender = "M"
SecondaryRecipient.IDNumber = "54111111"
SecondaryRecipient.IDType = "200"
SecondaryRecipient.LastName = "Doe"
SecondaryRecipient.MiddleName = "Michael"
SecondaryRecipient.Nationality = "ARG"
SecondaryRecipient.PhoneNumber1 = "+1 011 11111111"
SecondaryRecipient.PhoneNumber2 = "+1 011 22222222"

pspShippingDetails.SecondaryRecipient = SecondaryRecipient

Address = {}
Address.AdditionalInfo = "2 A"
Address.City = "Miami"
Address.Country = "USA"
Address.HouseNumber = "1245"
Address.StateProvince = "Florida"
Address.Street = "Av. Collins"
Address.ZipCode = "33140"

pspShippingDetails.Address = Address

authorize2p.psp_ShippingDetails = pspShippingDetails

response = nps.authorize_2p(authorize2p)

print(resp.psp_ResponseCod)
