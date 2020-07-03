SimpleQueryTxTransactions = {}

SimpleQueryTxTransactions.psp_ResponseCod = "2"
SimpleQueryTxTransactions.psp_ResponseMsg = "Transaccion exitosa - Aprobada"
SimpleQueryTxTransactions.psp_ResponseExtended = "Aprobada"
SimpleQueryTxTransactions.psp_TransactionId = "100022"
SimpleQueryTxTransactions.psp_MerchantId = "sdk_test"
SimpleQueryTxTransactions.psp_TxSource = "WEB"
SimpleQueryTxTransactions.psp_Operation = "TC - Autorizacion"
SimpleQueryTxTransactions.psp_MerchTxRef = "ORDER1000-1"
SimpleQueryTxTransactions.psp_MerchOrderId = "ORDER1000"
SimpleQueryTxTransactions.psp_MerchAdditionalRef = "ADDITIONAL-REF1234"
SimpleQueryTxTransactions.psp_Amount = "15050"
SimpleQueryTxTransactions.psp_NumPayments = "1"
SimpleQueryTxTransactions.psp_PaymentAmount = "10050"
SimpleQueryTxTransactions.psp_Currency = "032"
SimpleQueryTxTransactions.psp_Country = "ARG"
SimpleQueryTxTransactions.psp_Product = "14"
SimpleQueryTxTransactions.psp_AuthorizationCode = "352123"
SimpleQueryTxTransactions.psp_BatchNro = "1254"
SimpleQueryTxTransactions.psp_SequenceNumber = "64564321654"
SimpleQueryTxTransactions.psp_TicketNumber = "1254"
SimpleQueryTxTransactions.psp_CardNumber_FSD = "125478"
SimpleQueryTxTransactions.psp_CardNumber_LFD = "0001"
SimpleQueryTxTransactions.psp_CardMask = "451423XXXXXX1452"
SimpleQueryTxTransactions.psp_CardHolderName = "JOHN DOE"
SimpleQueryTxTransactions.psp_CustomerMail = "client@client.com.ar"
SimpleQueryTxTransactions.psp_CustomerId = "P123765"
SimpleQueryTxTransactions.psp_CustomerHttpUserAgent = " Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0"
SimpleQueryTxTransactions.psp_CustomerIpAddress = "200.123.123.100"
SimpleQueryTxTransactions.psp_MerchantMail = "merchant@merchant.com.ar"
SimpleQueryTxTransactions.psp_ClTrnId = "365258"
SimpleQueryTxTransactions.psp_ClExternalMerchant = "96878987"
SimpleQueryTxTransactions.psp_ClExternalTerminal = "14587986"
SimpleQueryTxTransactions.psp_ClResponseCod = "155"
SimpleQueryTxTransactions.psp_ClResponseMsg = "33140"
SimpleQueryTxTransactions.psp_PosDateTime = "2008-01-12 13:05:00"
SimpleQueryTxTransactions.psp_PurchaseDescription = "Com. X Art 1555"
SimpleQueryTxTransactions.psp_SoftDescriptor = "Compra Art 15"
SimpleQueryTxTransactions.psp_3dSecure_XID = "MjY0MjAxNjA4MDIyMDUzMzYyNjU="
SimpleQueryTxTransactions.psp_3dSecure_CAVV = "AAABBYZ3N5Qhl3kBU3c3ELGUsMY="
SimpleQueryTxTransactions.psp_3dSecure_Eci = "05"
SimpleQueryTxTransactions.psp_3dSecure_EciMsg = ""
SimpleQueryTxTransactions.psp_3dSecure_Secured = "1"
SimpleQueryTxTransactions.psp_3dSecure_ProtocolVersion = "2.1.0"
SimpleQueryTxTransactions.psp_3dSecure_DirectoryServerTransactionId = "c4e59ceb-a382-4d6a-bc87-385d591fa09d"
SimpleQueryTxTransactions.psp_CreatedAt = "2008-01-12 13:05:35-03:00"

pspAmountAdditionalDetails = {}
pspAmountAdditionalDetails.Tip = "20000"
pspAmountAdditionalDetails.Discount = "11000"

Taxes = {}

Taxes1 = {}
Taxes1.TypeId = "500"
Taxes1.Amount = "10000"
Taxes1.Rate = "2100"
Taxes1.BaseAmount = "10000"

Taxes[#Taxes+1] = Taxes1

Taxes2 = {}
Taxes2.TypeId = "500"
Taxes2.Amount = "10000"
Taxes2.Rate = "2100"
Taxes2.BaseAmount = "10000"

Taxes[#Taxes+1] = Taxes2

pspAmountAdditionalDetails.Taxes = Taxes

SimpleQueryTxTransactions.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspFraudScreeningResult = {}
pspFraudScreeningResult.ResultCode = "A"
pspFraudScreeningResult.ResultDescription = "ACCEPT"
pspFraudScreeningResult.AdditionalInfo = "Information"

SimpleQueryTxTransactions.psp_FraudScreeningResult = pspFraudScreeningResult

pspVerificationServicesResult = {}
pspVerificationServicesResult.ResultCodeCardSecurityCode = "M"
pspVerificationServicesResult.ResultCodeBillingAddress = "M"
pspVerificationServicesResult.ResultCodeBillingAddressZipCode = "M"
pspVerificationServicesResult.ResultCodeBillingPersonIDType = "M"
pspVerificationServicesResult.ResultCodeBillingPersonIDNumber = "M"
pspVerificationServicesResult.ResultCodeBillingPersonDateOfBirth = "M"
pspVerificationServicesResult.ResultCodeBillingPersonName = "M"
pspVerificationServicesResult.ResultCodeBillingPersonPhoneNumber1 = "M"
pspVerificationServicesResult.ResultCodeCustomerEmailAddress = "M"

SimpleQueryTxTransactions.psp_VerificationServicesResult = pspVerificationServicesResult

pspMerchantAdditionalDetails = {}
pspMerchantAdditionalDetails.Type = "2 A"

SellerDetails = {}
SellerDetails.IDNumber = "30706033471"
SellerDetails.IDType = "205"
SellerDetails.Name = "Company S.A."
SellerDetails.Invoice = "54877555"
SellerDetails.PurchaseDescription = "Samsung 4K SUHD TV"

Address = {}
Address.AdditionalInfo = "2 A"
Address.City = "Miami"
Address.Country = "USA"
Address.HouseNumber = "1245"
Address.StateProvince = "Florida"
Address.Street = "Av. Collins"
Address.ZipCode = "33140"

SellerDetails.Address = Address
SellerDetails.MCC = "5732"
SellerDetails.ChannelCode = ""
SellerDetails.GeoCode = ""

pspMerchantAdditionalDetails.SellerDetails = SellerDetails

SimpleQueryTxTransactions.psp_MerchantAdditionalDetails = pspMerchantAdditionalDetails

pspCustomerAdditionalDetails = {}
pspCustomerAdditionalDetails.EmailAddress = "jdoe@email.com"
pspCustomerAdditionalDetails.AlternativeEmailAddress = "Jdoe79@email.com"
pspCustomerAdditionalDetails.IPAddress = "192.168.158.190"
pspCustomerAdditionalDetails.AccountID = "Jdoe78"
pspCustomerAdditionalDetails.AccountCreatedAt = "2010-10-23"
pspCustomerAdditionalDetails.AccountPreviousActivity = "1"
pspCustomerAdditionalDetails.AccountHasCredentials = "1"
pspCustomerAdditionalDetails.DeviceType = "1"
pspCustomerAdditionalDetails.DeviceFingerPrint = "KJhKHKJgh7777kgh"
pspCustomerAdditionalDetails.BrowserLanguage = "ES"
pspCustomerAdditionalDetails.HttpUserAgent = "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0"

SimpleQueryTxTransactions.psp_CustomerAdditionalDetails = pspCustomerAdditionalDetails

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

SimpleQueryTxTransactions.psp_BillingDetails = pspBillingDetails

pspShippingDetails = {}
pspShippingDetails.TrackingNumber = "154DDD54DWW11"
pspShippingDetails.Method = "1"
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

SimpleQueryTxTransactions.psp_ShippingDetails = pspShippingDetails

pspOrderDetails = {}

pspOrderDetails1 = {}
pspOrderDetails1.Quantity = "10"
pspOrderDetails1.UnitPrice = "10050"
pspOrderDetails1.Description = "Blue pencil"
pspOrderDetails1.Type = "1002"
pspOrderDetails1.SkuCode = "SO-4587885545"
pspOrderDetails1.ManufacturerPartNumber = "CN-0N2828421-3AD-02CD"
pspOrderDetails1.Risk = "H"

pspOrderDetails[#pspOrderDetails+1] = pspOrderDetails1

pspOrderDetails2 = {}
pspOrderDetails2.Quantity = "10"
pspOrderDetails2.UnitPrice = "10050"
pspOrderDetails2.Description = "Blue pencil"
pspOrderDetails2.Type = "1002"
pspOrderDetails2.SkuCode = "SO-4587885545"
pspOrderDetails2.ManufacturerPartNumber = "CN-0N2828421-3AD-02CD"
pspOrderDetails2.Risk = "H"

pspOrderDetails[#pspOrderDetails+1] = pspOrderDetails2

SimpleQueryTxTransactions.psp_OrderDetails = pspOrderDetails

pspAirlineDetails = {}
pspAirlineDetails.PNR = "154DDD54DWW11"

Legs = {}

Legs1 = {}
Legs1.DepartureAirport = "EZE"
Legs1.DepartureDatetime = "2014-05-12 13:05:00"
Legs1.DepartureAirportTimezone = "-03:00"
Legs1.ArrivalAirport = "AMS"
Legs1.CarrierCode = "KL"
Legs1.FlightNumber = "842"
Legs1.FareBasisCode = "HL7LNR"
Legs1.FareClassCode = "FR"
Legs1.BaseFare = "30000"
Legs1.BaseFareCurrency = "032"

Legs[#Legs+1] = Legs1

pspAirlineDetails.Legs = Legs

Passengers = {}

Passengers1 = {}
Passengers1.FirstName = "John"
Passengers1.LastName = "Doe"
Passengers1.MiddleName = "Michael"
Passengers1.Type = "A"
Passengers1.DateOfBirth = "1979-01-12"
Passengers1.Nationality = "ARG"
Passengers1.IDNumber = "54111111"
Passengers1.IDType = "100"
Passengers1.IDCountry = "ARG"
Passengers1.LoyaltyNumber = "254587547"
Passengers1.LoyaltyTier = "1"

Passengers[#Passengers+1] = Passengers1

pspAirlineDetails.Passengers = Passengers

Ticket = {}
Ticket.TicketNumber = "07411865255578"
Ticket.Eticket = "1"
Ticket.Restricted = "1"

Issue = {}
Issue.TravelAgentCode = "32165464"
Issue.TravelAgentName = "Washington Hilton"
Issue.Date = "2017-01-10"
Issue.Country = "ARG"
Issue.City = "Buenos Aires"
Issue.Address = "Av. Rivadavia 1111"

Ticket.Issue = Issue
Ticket.TotalFareAmount = "80000"
Ticket.TotalTaxAmount = "25200"
Ticket.TotalFeeAmount = "14800"

pspAirlineDetails.Ticket = Ticket

SimpleQueryTxTransactions.psp_AirlineDetails = pspAirlineDetails
