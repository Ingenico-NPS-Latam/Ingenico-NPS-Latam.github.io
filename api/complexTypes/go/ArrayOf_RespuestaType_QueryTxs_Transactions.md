ArrayOfQueryTxsTransactions := nps.NewArrayOfQueryTxsTransactionsStruct()
ArrayOfQueryTxsTransactions.Psp_ResponseCod = "2"
ArrayOfQueryTxsTransactions.Psp_ResponseMsg = "Transaccion exitosa - Aprobada"
ArrayOfQueryTxsTransactions.Psp_ResponseExtended = "Aprobada"
ArrayOfQueryTxsTransactions.Psp_TransactionId = "100022"
ArrayOfQueryTxsTransactions.Psp_MerchantId = "sdk_test"
ArrayOfQueryTxsTransactions.Psp_TxSource = "WEB"
ArrayOfQueryTxsTransactions.Psp_Operation = "TC  Autorizacion"
ArrayOfQueryTxsTransactions.Psp_MerchTxRef = "ORDER1000-1"
ArrayOfQueryTxsTransactions.Psp_MerchOrderId = "ORDER1000"
ArrayOfQueryTxsTransactions.Psp_MerchAdditionalRef = "ADDITIONAL-REF1234"
ArrayOfQueryTxsTransactions.Psp_Amount = "15050"
ArrayOfQueryTxsTransactions.Psp_NumPayments = "1"
ArrayOfQueryTxsTransactions.Psp_PaymentAmount = "10050"
ArrayOfQueryTxsTransactions.Psp_Currency = "032"
ArrayOfQueryTxsTransactions.Psp_Country = "ARG"
ArrayOfQueryTxsTransactions.Psp_Product = "14"
ArrayOfQueryTxsTransactions.Psp_AuthorizationCode = "352123"
ArrayOfQueryTxsTransactions.Psp_BatchNro = "1254"
ArrayOfQueryTxsTransactions.Psp_SequenceNumber = "64564321654"
ArrayOfQueryTxsTransactions.Psp_TicketNumber = "1254"
ArrayOfQueryTxsTransactions.Psp_CardNumber_FSD = "125478"
ArrayOfQueryTxsTransactions.Psp_CardNumber_LFD = "0001"
ArrayOfQueryTxsTransactions.Psp_CardMask = "451423XXXXXX1452"
ArrayOfQueryTxsTransactions.Psp_CardHolderName = "JOHN DOE"
ArrayOfQueryTxsTransactions.Psp_CustomerMail = "client@client.com.ar"
ArrayOfQueryTxsTransactions.Psp_CustomerId = "P123765"
ArrayOfQueryTxsTransactions.Psp_CustomerHttpUserAgent = " Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0"
ArrayOfQueryTxsTransactions.Psp_CustomerIpAddress = "200.123.123.100"
ArrayOfQueryTxsTransactions.Psp_MerchantMail = "merchant@merchant.com.ar"
ArrayOfQueryTxsTransactions.Psp_ClTrnId = "365258"
ArrayOfQueryTxsTransactions.Psp_ClExternalMerchant = "96878987"
ArrayOfQueryTxsTransactions.Psp_ClExternalTerminal = "14587986"
ArrayOfQueryTxsTransactions.Psp_ClResponseCod = "155"
ArrayOfQueryTxsTransactions.Psp_ClResponseMsg = "33140"
ArrayOfQueryTxsTransactions.Psp_PosDateTime = "2008-01-12 13:05:00"
ArrayOfQueryTxsTransactions.Psp_PurchaseDescription = "Com. X Art 1555"
ArrayOfQueryTxsTransactions.Psp_SoftDescriptor = "Compra Art 15"
ArrayOfQueryTxsTransactions.Psp_Plan = "PlanZ"
ArrayOfQueryTxsTransactions.Psp_3dSecure_XID = "MjY0MjAxNjA4MDIyMDUzMzYyNjU="
ArrayOfQueryTxsTransactions.Psp_3dSecure_CAVV = "AAABBYZ3N5Qhl3kBU3c3ELGUsMY="
ArrayOfQueryTxsTransactions.Psp_3dSecure_Eci = "05"
ArrayOfQueryTxsTransactions.Psp_3dSecure_EciMsg = ""
ArrayOfQueryTxsTransactions.Psp_3dSecure_Secured = "1"
ArrayOfQueryTxsTransactions.Psp_CreatedAt = "2008-01-12 13:05:35-03:00"
ArrayOfQueryTxsTransactions.psp_3dSecure_ProtocolVersion = "2.1.0"
ArrayOfQueryTxsTransactions.psp_3dSecure_DirectoryServerTransactionId = "c4e59ceb-a382-4d6a-bc87-385d591fa09d"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsRequestStruct()
pspAmountAdditionalDetails.Tip = "20000"
pspAmountAdditionalDetails.Discount = "11000"

Taxes := nps.NewArrayOf_TaxesRequestStruct()
Taxes.Items = make([]*nps.NewTaxesRequestStruct(), 0)

Taxes1 := nps.NewTaxesRequestStruct()
Taxes1.TypeId = "500"
Taxes1.Amount = "10000"
Taxes1.Rate = "2100"
Taxes1.BaseAmount = "10000"
Taxes.Items = append(Taxes.Items, Taxes1)

Taxes2 := nps.NewTaxesRequestStruct()
Taxes2.TypeId = "500"
Taxes2.Amount = "10000"
Taxes2.Rate = "2100"
Taxes2.BaseAmount = "10000"
Taxes.Items = append(Taxes.Items, Taxes2)


ArrayOfQueryTxsTransactions.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspFraudScreeningResult := nps.NewFraudScreeningResultStruct()
pspFraudScreeningResult.ResultCode = "A"
pspFraudScreeningResult.ResultDescription = "ACCEPT"
pspFraudScreeningResult.AdditionalInfo = "Information"

ArrayOfQueryTxsTransactions.psp_FraudScreeningResult = pspFraudScreeningResult

pspVerificationServicesResult := nps.NewVerificationServicesResultStruct()
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

pspMerchantAdditionalDetails := nps.NewMerchantAdditionalDetailsStruct()
pspMerchantAdditionalDetails.Type = "2 A"

SellerDetails := nps.NewSellerDetailsStruct()
SellerDetails.IDNumber = "30706033471"
SellerDetails.IDType = "205"
SellerDetails.Name = "Company S.A."
SellerDetails.Invoice = "54877555"
SellerDetails.PurchaseDescription = "Samsung 4K SUHD TV"

Address := nps.NewAddressStruct()
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

pspCustomerAdditionalDetails := nps.NewCustomerAdditionalDetailsStruct()
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

pspBillingDetails := nps.NewBillingDetailsStruct()
pspBillingDetails.Invoice = "54877555"
pspBillingDetails.InvoiceDate = "2017-10-23"
pspBillingDetails.InvoiceAmount = "15050"
pspBillingDetails.InvoiceCurrency = "032"

Person := nps.NewPersonStruct()
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

Address := nps.NewAddressStruct()
Address.AdditionalInfo = "2 A"
Address.City = "Miami"
Address.Country = "USA"
Address.HouseNumber = "1245"
Address.StateProvince = "Florida"
Address.Street = "Av. Collins"
Address.ZipCode = "33140"

pspBillingDetails.Address = Address

ArrayOfQueryTxsTransactions.psp_BillingDetails = pspBillingDetails

pspShippingDetails := nps.NewShippingDetailsStruct()
pspShippingDetails.TrackingNumber = "154DDD54DWW11"
pspShippingDetails.Method = "1"
pspShippingDetails.Carrier = "200"
pspShippingDetails.DeliveryDate = "2014-11-20"
pspShippingDetails.FreightAmount = "15000"
pspShippingDetails.GiftMessage = "Happy Birthday!"
pspShippingDetails.GiftWrapping = "1"

PrimaryRecipient := nps.NewPrimaryRecipientStruct()
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

SecondaryRecipient := nps.NewSecondaryRecipientStruct()
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

Address := nps.NewAddressStruct()
Address.AdditionalInfo = "2 A"
Address.City = "Miami"
Address.Country = "USA"
Address.HouseNumber = "1245"
Address.StateProvince = "Florida"
Address.Street = "Av. Collins"
Address.ZipCode = "33140"

pspShippingDetails.Address = Address

ArrayOfQueryTxsTransactions.psp_ShippingDetails = pspShippingDetails

pspOrderDetails := nps.NewArrayOf_OrderDetailsStruct()
pspOrderDetails.Items = make([]*nps.NewOrderDetailsStruct(), 0)

pspOrderDetails1 := nps.NewpspOrderDetailsStruct()
pspOrderDetails1.Quantity = "10"
pspOrderDetails1.UnitPrice = "10050"
pspOrderDetails1.Description = "Blue pencil"
pspOrderDetails1.Type = "1002"
pspOrderDetails1.SkuCode = "SO-4587885545"
pspOrderDetails1.ManufacturerPartNumber = "CN-0N2828421-3AD-02CD"
pspOrderDetails1.Risk = "H"
pspOrderDetails.Items = append(pspOrderDetails.Items, pspOrderDetails1)

pspOrderDetails2 := nps.NewpspOrderDetailsStruct()
pspOrderDetails2.Quantity = "10"
pspOrderDetails2.UnitPrice = "10050"
pspOrderDetails2.Description = "Blue pencil"
pspOrderDetails2.Type = "1002"
pspOrderDetails2.SkuCode = "SO-4587885545"
pspOrderDetails2.ManufacturerPartNumber = "CN-0N2828421-3AD-02CD"
pspOrderDetails2.Risk = "H"
pspOrderDetails.Items = append(pspOrderDetails.Items, pspOrderDetails2)


pspAirlineDetails := nps.NewAirlineDetailsStruct()
pspAirlineDetails.PNR = "154DDD54DWW11"

Legs := nps.NewArrayOf_LegsStruct()
Legs.Items = make([]*nps.NewLegsStruct(), 0)

Legs1 := nps.NewLegsStruct()
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
Legs.Items = append(Legs.Items, Legs1)


Passengers := nps.NewArrayOf_PassengersStruct()
Passengers.Items = make([]*nps.NewPassengersStruct(), 0)

Passengers1 := nps.NewPassengersStruct()
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
Passengers.Items = append(Passengers.Items, Passengers1)


Ticket := nps.NewTicketStruct()
Ticket.TicketNumber = "07411865255578"
Ticket.Eticket = "1"
Ticket.Restricted = "1"

Issue := nps.NewIssueStruct()
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
