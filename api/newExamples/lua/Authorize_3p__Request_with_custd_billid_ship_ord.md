local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


authorize3p = {}

authorize3p.psp_Version = "2.2"
authorize3p.psp_MerchantId = "sdk_test"
authorize3p.psp_TxSource = "WEB"
authorize3p.psp_MerchTxRef = "ORDER76666-3"
authorize3p.psp_MerchOrderId = "ORDER76666"
authorize3p.psp_ReturnURL = "http://localhost/"
authorize3p.psp_FrmLanguage = "es_AR"
authorize3p.psp_Amount = "15050"
authorize3p.psp_NumPayments = "1"
authorize3p.psp_Currency = "032"
authorize3p.psp_Country = "ARG"
authorize3p.psp_Product = "14"
authorize3p.psp_PosDateTime = "2019-12-01 12:00:00"

pspCustomerAdditionalDetails = {}
pspCustomerAdditionalDetails.EmailAddress = "jdoe@email.com"
pspCustomerAdditionalDetails.AlternativeEmailAddress = "Jdoe79@email.com"
pspCustomerAdditionalDetails.IPAddress = "192.168.158.190"
pspCustomerAdditionalDetails.AccountID = "Jdoe78"
pspCustomerAdditionalDetails.AccountCreatedAt = "2010-10-23"
pspCustomerAdditionalDetails.AccountPreviousActivity = "1"
pspCustomerAdditionalDetails.AccountHasCredentials = "1"
pspCustomerAdditionalDetails.DeviceType = "1"
pspCustomerAdditionalDetails.DeviceFingerPrint = "KJhKHKJgh7777kgh..."
pspCustomerAdditionalDetails.BrowserLanguage = "ES"
pspCustomerAdditionalDetails.HttpUserAgent = "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0"

authorize3p.psp_CustomerAdditionalDetails = pspCustomerAdditionalDetails

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

authorize3p.psp_BillingDetails = pspBillingDetails

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

authorize3p.psp_ShippingDetails = pspShippingDetails

pspOrderDetails = {}

OrderItems = {}

OrderItems1 = {}
OrderItems1.Quantity = "10"
OrderItems1.UnitPrice = "10050"
OrderItems1.Description = "Blue pencil"
OrderItems1.Type = "1002"
OrderItems1.SkuCode = "SO-4587885545"
OrderItems1.ManufacturerPartNumber = "CN-0N2828421-3AD-02CD"
OrderItems1.Risk = "H"

OrderItems[#OrderItems+1] = OrderItems1

pspOrderDetails.OrderItems = OrderItems

authorize3p.psp_OrderDetails = pspOrderDetails

response = nps.authorize_3p(authorize3p)

print(resp.psp_ResponseCod)
