ArrayOfQueryTxsTransactions = {}

ArrayOfQueryTxsTransactions.psp_ResponseCod = "2"
ArrayOfQueryTxsTransactions.psp_ResponseMsg = "Transaccion exitosa - Aprobada"
ArrayOfQueryTxsTransactions.psp_ResponseExtended = "Aprobada"
ArrayOfQueryTxsTransactions.psp_TransactionId = "100022"
ArrayOfQueryTxsTransactions.psp_MerchantId = "sdk_test"
ArrayOfQueryTxsTransactions.psp_TxSource = "WEB"
ArrayOfQueryTxsTransactions.psp_Operation = "TC  Autorizacion"
ArrayOfQueryTxsTransactions.psp_MerchTxRef = "ORDER1000-1"
ArrayOfQueryTxsTransactions.psp_MerchOrderId = "ORDER1000"
ArrayOfQueryTxsTransactions.psp_MerchAdditionalRef = "ADDITIONAL-REF1234"
ArrayOfQueryTxsTransactions.psp_Amount = "15050"
ArrayOfQueryTxsTransactions.psp_NumPayments = "1"
ArrayOfQueryTxsTransactions.psp_PaymentAmount = "10050"
ArrayOfQueryTxsTransactions.psp_Currency = "032"
ArrayOfQueryTxsTransactions.psp_Country = "ARG"
ArrayOfQueryTxsTransactions.psp_Product = "14"
ArrayOfQueryTxsTransactions.psp_AuthorizationCode = "352123"
ArrayOfQueryTxsTransactions.psp_BatchNro = "1254"
ArrayOfQueryTxsTransactions.psp_SequenceNumber = "64564321654"
ArrayOfQueryTxsTransactions.psp_TicketNumber = "1254"
ArrayOfQueryTxsTransactions.psp_CardNumber_FSD = "125478"
ArrayOfQueryTxsTransactions.psp_CardNumber_LFD = "0001"
ArrayOfQueryTxsTransactions.psp_CardMask = "451423XXXXXX1452"
ArrayOfQueryTxsTransactions.psp_CardHolderName = "JOHN DOE"
ArrayOfQueryTxsTransactions.psp_CustomerMail = "client@client.com.ar"
ArrayOfQueryTxsTransactions.psp_CustomerId = "P123765"
ArrayOfQueryTxsTransactions.psp_CustomerHttpUserAgent = " Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0"
ArrayOfQueryTxsTransactions.psp_CustomerIpAddress = "200.123.123.100"
ArrayOfQueryTxsTransactions.psp_MerchantMail = "merchant@merchant.com.ar"
ArrayOfQueryTxsTransactions.psp_ClTrnId = "365258"
ArrayOfQueryTxsTransactions.psp_ClExternalMerchant = "96878987"
ArrayOfQueryTxsTransactions.psp_ClExternalTerminal = "14587986"
ArrayOfQueryTxsTransactions.psp_ClResponseCod = "155"
ArrayOfQueryTxsTransactions.psp_ClResponseMsg = "33140"
ArrayOfQueryTxsTransactions.psp_PosDateTime = "2008-01-12 13:05:00"
ArrayOfQueryTxsTransactions.psp_PurchaseDescription = "Com. X Art 1555"
ArrayOfQueryTxsTransactions.psp_SoftDescriptor = "Compra Art 15"
ArrayOfQueryTxsTransactions.psp_Plan = "PlanZ"
ArrayOfQueryTxsTransactions.psp_3dSecure_XID = "MjY0MjAxNjA4MDIyMDUzMzYyNjU="
ArrayOfQueryTxsTransactions.psp_3dSecure_CAVV = "AAABBYZ3N5Qhl3kBU3c3ELGUsMY="
ArrayOfQueryTxsTransactions.psp_3dSecure_Eci = "05"
ArrayOfQueryTxsTransactions.psp_3dSecure_EciMsg = ""
ArrayOfQueryTxsTransactions.psp_3dSecure_Secured = "1"
ArrayOfQueryTxsTransactions.psp_3dSecure_ProtocolVersion = "2.1.0"
ArrayOfQueryTxsTransactions.psp_3dSecure_DirectoryServerTransactionId = "c4e59ceb-a382-4d6a-bc87-385d591fa09d"
ArrayOfQueryTxsTransactions.psp_CreatedAt = "2008-01-12 13:05:35-03:00"

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

ArrayOfQueryTxsTransactions.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspFraudScreeningResult = {}
pspFraudScreeningResult.ResultCode = "A"
pspFraudScreeningResult.ResultDescription = "ACCEPT"
pspFraudScreeningResult.AdditionalInfo = "Information"

ArrayOfQueryTxsTransactions.psp_FraudScreeningResult = pspFraudScreeningResult

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

ArrayOfQueryTxsTransactions.psp_VerificationServicesResult = pspVerificationServicesResult

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

ArrayOfQueryTxsTransactions.psp_MerchantAdditionalDetails = pspMerchantAdditionalDetails

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

ArrayOfQueryTxsTransactions.psp_CustomerAdditionalDetails = pspCustomerAdditionalDetails

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

ArrayOfQueryTxsTransactions.psp_BillingDetails = pspBillingDetails

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

ArrayOfQueryTxsTransactions.psp_ShippingDetails = pspShippingDetails

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

ArrayOfQueryTxsTransactions.psp_OrderDetails = pspOrderDetails

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
Issue.CarrierCode = "AA"
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

ArrayOfQueryTxsTransactions.psp_AirlineDetails = pspAirlineDetails
