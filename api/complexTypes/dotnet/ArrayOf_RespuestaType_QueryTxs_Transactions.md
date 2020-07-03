RootElement data = new RootElement();

data.Add("psp_ResponseCod", "2");
data.Add("psp_ResponseMsg", "Transaccion exitosa - Aprobada");
data.Add("psp_ResponseExtended", "Aprobada");
data.Add("psp_TransactionId", "100022");
data.Add("psp_MerchantId", "sdk_test");
data.Add("psp_TxSource", "WEB");
data.Add("psp_Operation", "TC  Autorizacion");
data.Add("psp_MerchTxRef", "ORDER1000-1");
data.Add("psp_MerchOrderId", "ORDER1000");
data.Add("psp_MerchAdditionalRef", "ADDITIONAL-REF1234");
data.Add("psp_Amount", "15050");
data.Add("psp_NumPayments", "1");
data.Add("psp_PaymentAmount", "10050");
data.Add("psp_Currency", "032");
data.Add("psp_Country", "ARG");
data.Add("psp_Product", "14");
data.Add("psp_AuthorizationCode", "352123");
data.Add("psp_BatchNro", "1254");
data.Add("psp_SequenceNumber", "64564321654");
data.Add("psp_TicketNumber", "1254");
data.Add("psp_CardNumber_FSD", "125478");
data.Add("psp_CardNumber_LFD", "0001");
data.Add("psp_CardMask", "451423XXXXXX1452");
data.Add("psp_CardHolderName", "JOHN DOE");
data.Add("psp_CustomerMail", "client@client.com.ar");
data.Add("psp_CustomerId", "P123765");
data.Add("psp_CustomerHttpUserAgent", " Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0");
data.Add("psp_CustomerIpAddress", "200.123.123.100");
data.Add("psp_MerchantMail", "merchant@merchant.com.ar");
data.Add("psp_ClTrnId", "365258");
data.Add("psp_ClExternalMerchant", "96878987");
data.Add("psp_ClExternalTerminal", "14587986");
data.Add("psp_ClResponseCod", "155");
data.Add("psp_ClResponseMsg", "33140");
data.Add("psp_PosDateTime", "2008-01-12 13:05:00");
data.Add("psp_PurchaseDescription", "Com. X Art 1555");
data.Add("psp_SoftDescriptor", "Compra Art 15");
data.Add("psp_Plan", "PlanZ");
data.Add("psp_3dSecure_XID", "MjY0MjAxNjA4MDIyMDUzMzYyNjU=");
data.Add("psp_3dSecure_CAVV", "AAABBYZ3N5Qhl3kBU3c3ELGUsMY=");
data.Add("psp_3dSecure_Eci", "05");
data.Add("psp_3dSecure_EciMsg", "");
data.Add("psp_3dSecure_Secured", "1");
data.Add("psp_3dSecure_ProtocolVersion", "2.1.0");
data.Add("psp_3dSecure_DirectoryServerTransactionId", "c4e59ceb-a382-4d6a-bc87-385d591fa09d");
data.Add("psp_CreatedAt", "2008-01-12 13:05:35-03:00");

ComplexElement pspAmountAdditionalDetails = new ComplexElement();
pspAmountAdditionalDetails.Add("Tip", "20000");
pspAmountAdditionalDetails.Add("Discount", "11000");

ComplexElementArray Taxes = new ComplexElementArray();

ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
Taxes1.Add("TypeId", "500");
Taxes1.Add("Amount", "10000");
Taxes1.Add("Rate", "2100");
Taxes1.Add("BaseAmount", "10000");

Taxes.Add(Taxes1);

ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
Taxes2.Add("TypeId", "500");
Taxes2.Add("Amount", "10000");
Taxes2.Add("Rate", "2100");
Taxes2.Add("BaseAmount", "10000");

Taxes.Add(Taxes2);

pspAmountAdditionalDetails.Add("Taxes", Taxes);

data.Add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);

ComplexElement pspFraudScreeningResult = new ComplexElement();
pspFraudScreeningResult.Add("ResultCode", "A");
pspFraudScreeningResult.Add("ResultDescription", "ACCEPT");
pspFraudScreeningResult.Add("AdditionalInfo", "Information");

data.Add("psp_FraudScreeningResult", pspFraudScreeningResult);

ComplexElement pspVerificationServicesResult = new ComplexElement();
pspVerificationServicesResult.Add("ResultCodeCardSecurityCode", "M");
pspVerificationServicesResult.Add("ResultCodeBillingAddress", "M");
pspVerificationServicesResult.Add("ResultCodeBillingAddressZipCode", "M");
pspVerificationServicesResult.Add("ResultCodeBillingPersonIDType", "M");
pspVerificationServicesResult.Add("ResultCodeBillingPersonIDNumber", "M");
pspVerificationServicesResult.Add("ResultCodeBillingPersonDateOfBirth", "M");
pspVerificationServicesResult.Add("ResultCodeBillingPersonName", "M");
pspVerificationServicesResult.Add("ResultCodeBillingPersonPhoneNumber1", "M");
pspVerificationServicesResult.Add("ResultCodeCustomerEmailAddress", "M");

data.Add("psp_VerificationServicesResult", pspVerificationServicesResult);

ComplexElement pspMerchantAdditionalDetails = new ComplexElement();
pspMerchantAdditionalDetails.Add("Type", "2 A");

ComplexElement SellerDetails = new ComplexElement();
SellerDetails.Add("IDNumber", "30706033471");
SellerDetails.Add("IDType", "205");
SellerDetails.Add("Name", "Company S.A.");
SellerDetails.Add("Invoice", "54877555");
SellerDetails.Add("PurchaseDescription", "Samsung 4K SUHD TV");

ComplexElement Address = new ComplexElement();
Address.Add("AdditionalInfo", "2 A");
Address.Add("City", "Miami");
Address.Add("Country", "USA");
Address.Add("HouseNumber", "1245");
Address.Add("StateProvince", "Florida");
Address.Add("Street", "Av. Collins");
Address.Add("ZipCode", "33140");

SellerDetails.Add("Address", Address);
SellerDetails.Add("MCC", "5732");
SellerDetails.Add("ChannelCode", "");
SellerDetails.Add("GeoCode", "");

pspMerchantAdditionalDetails.Add("SellerDetails", SellerDetails);

data.Add("psp_MerchantAdditionalDetails", pspMerchantAdditionalDetails);

ComplexElement pspCustomerAdditionalDetails = new ComplexElement();
pspCustomerAdditionalDetails.Add("EmailAddress", "jdoe@email.com");
pspCustomerAdditionalDetails.Add("AlternativeEmailAddress", "Jdoe79@email.com");
pspCustomerAdditionalDetails.Add("IPAddress", "192.168.158.190");
pspCustomerAdditionalDetails.Add("AccountID", "Jdoe78");
pspCustomerAdditionalDetails.Add("AccountCreatedAt", "2010-10-23");
pspCustomerAdditionalDetails.Add("AccountPreviousActivity", "1");
pspCustomerAdditionalDetails.Add("AccountHasCredentials", "1");
pspCustomerAdditionalDetails.Add("DeviceType", "1");
pspCustomerAdditionalDetails.Add("DeviceFingerPrint", "KJhKHKJgh7777kgh");
pspCustomerAdditionalDetails.Add("BrowserLanguage", "ES");
pspCustomerAdditionalDetails.Add("HttpUserAgent", "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0");

data.Add("psp_CustomerAdditionalDetails", pspCustomerAdditionalDetails);

ComplexElement pspBillingDetails = new ComplexElement();
pspBillingDetails.Add("Invoice", "54877555");
pspBillingDetails.Add("InvoiceDate", "2017-10-23");
pspBillingDetails.Add("InvoiceAmount", "15050");
pspBillingDetails.Add("InvoiceCurrency", "032");

ComplexElement Person = new ComplexElement();
Person.Add("DateOfBirth", "1979-01-12");
Person.Add("FirstName", "John");
Person.Add("Gender", "M");
Person.Add("IDNumber", "54111111");
Person.Add("IDType", "200");
Person.Add("LastName", "Doe");
Person.Add("MiddleName", "Michael");
Person.Add("Nationality", "ARG");
Person.Add("PhoneNumber1", "+1 011 11111111");
Person.Add("PhoneNumber2", "+1 011 22222222");

pspBillingDetails.Add("Person", Person);

ComplexElement Address = new ComplexElement();
Address.Add("AdditionalInfo", "2 A");
Address.Add("City", "Miami");
Address.Add("Country", "USA");
Address.Add("HouseNumber", "1245");
Address.Add("StateProvince", "Florida");
Address.Add("Street", "Av. Collins");
Address.Add("ZipCode", "33140");

pspBillingDetails.Add("Address", Address);

data.Add("psp_BillingDetails", pspBillingDetails);

ComplexElement pspShippingDetails = new ComplexElement();
pspShippingDetails.Add("TrackingNumber", "154DDD54DWW11");
pspShippingDetails.Add("Method", "1");
pspShippingDetails.Add("Carrier", "200");
pspShippingDetails.Add("DeliveryDate", "2014-11-20");
pspShippingDetails.Add("FreightAmount", "15000");
pspShippingDetails.Add("GiftMessage", "Happy Birthday!");
pspShippingDetails.Add("GiftWrapping", "1");

ComplexElement PrimaryRecipient = new ComplexElement();
PrimaryRecipient.Add("DateOfBirth", "1979-01-12");
PrimaryRecipient.Add("FirstName", "John");
PrimaryRecipient.Add("Gender", "M");
PrimaryRecipient.Add("IDNumber", "54111111");
PrimaryRecipient.Add("IDType", "200");
PrimaryRecipient.Add("LastName", "Doe");
PrimaryRecipient.Add("MiddleName", "Michael");
PrimaryRecipient.Add("Nationality", "ARG");
PrimaryRecipient.Add("PhoneNumber1", "+1 011 11111111");
PrimaryRecipient.Add("PhoneNumber2", "+1 011 22222222");

pspShippingDetails.Add("PrimaryRecipient", PrimaryRecipient);

ComplexElement SecondaryRecipient = new ComplexElement();
SecondaryRecipient.Add("DateOfBirth", "1979-01-12");
SecondaryRecipient.Add("FirstName", "John");
SecondaryRecipient.Add("Gender", "M");
SecondaryRecipient.Add("IDNumber", "54111111");
SecondaryRecipient.Add("IDType", "200");
SecondaryRecipient.Add("LastName", "Doe");
SecondaryRecipient.Add("MiddleName", "Michael");
SecondaryRecipient.Add("Nationality", "ARG");
SecondaryRecipient.Add("PhoneNumber1", "+1 011 11111111");
SecondaryRecipient.Add("PhoneNumber2", "+1 011 22222222");

pspShippingDetails.Add("SecondaryRecipient", SecondaryRecipient);

ComplexElement Address = new ComplexElement();
Address.Add("AdditionalInfo", "2 A");
Address.Add("City", "Miami");
Address.Add("Country", "USA");
Address.Add("HouseNumber", "1245");
Address.Add("StateProvince", "Florida");
Address.Add("Street", "Av. Collins");
Address.Add("ZipCode", "33140");

pspShippingDetails.Add("Address", Address);

data.Add("psp_ShippingDetails", pspShippingDetails);

ComplexElementArray pspOrderDetails = new ComplexElementArray();

ComplexElementArrayItem pspOrderDetails1 = new ComplexElementArrayItem();
pspOrderDetails1.Add("Quantity", "10");
pspOrderDetails1.Add("UnitPrice", "10050");
pspOrderDetails1.Add("Description", "Blue pencil");
pspOrderDetails1.Add("Type", "1002");
pspOrderDetails1.Add("SkuCode", "SO-4587885545");
pspOrderDetails1.Add("ManufacturerPartNumber", "CN-0N2828421-3AD-02CD");
pspOrderDetails1.Add("Risk", "H");

pspOrderDetails.Add(pspOrderDetails1);

ComplexElementArrayItem pspOrderDetails2 = new ComplexElementArrayItem();
pspOrderDetails2.Add("Quantity", "10");
pspOrderDetails2.Add("UnitPrice", "10050");
pspOrderDetails2.Add("Description", "Blue pencil");
pspOrderDetails2.Add("Type", "1002");
pspOrderDetails2.Add("SkuCode", "SO-4587885545");
pspOrderDetails2.Add("ManufacturerPartNumber", "CN-0N2828421-3AD-02CD");
pspOrderDetails2.Add("Risk", "H");

pspOrderDetails.Add(pspOrderDetails2);

data.Add("psp_OrderDetails", pspOrderDetails);

ComplexElement pspAirlineDetails = new ComplexElement();
pspAirlineDetails.Add("PNR", "154DDD54DWW11");

ComplexElementArray Legs = new ComplexElementArray();

ComplexElementArrayItem Legs1 = new ComplexElementArrayItem();
Legs1.Add("DepartureAirport", "EZE");
Legs1.Add("DepartureDatetime", "2014-05-12 13:05:00");
Legs1.Add("DepartureAirportTimezone", "-03:00");
Legs1.Add("ArrivalAirport", "AMS");
Legs1.Add("CarrierCode", "KL");
Legs1.Add("FlightNumber", "842");
Legs1.Add("FareBasisCode", "HL7LNR");
Legs1.Add("FareClassCode", "FR");
Legs1.Add("BaseFare", "30000");
Legs1.Add("BaseFareCurrency", "032");

Legs.Add(Legs1);

pspAirlineDetails.Add("Legs", Legs);

ComplexElementArray Passengers = new ComplexElementArray();

ComplexElementArrayItem Passengers1 = new ComplexElementArrayItem();
Passengers1.Add("FirstName", "John");
Passengers1.Add("LastName", "Doe");
Passengers1.Add("MiddleName", "Michael");
Passengers1.Add("Type", "A");
Passengers1.Add("DateOfBirth", "1979-01-12");
Passengers1.Add("Nationality", "ARG");
Passengers1.Add("IDNumber", "54111111");
Passengers1.Add("IDType", "100");
Passengers1.Add("IDCountry", "ARG");
Passengers1.Add("LoyaltyNumber", "254587547");
Passengers1.Add("LoyaltyTier", "1");

Passengers.Add(Passengers1);

pspAirlineDetails.Add("Passengers", Passengers);

ComplexElement Ticket = new ComplexElement();
Ticket.Add("TicketNumber", "07411865255578");
Ticket.Add("Eticket", "1");
Ticket.Add("Restricted", "1");

ComplexElement Issue = new ComplexElement();
Issue.Add("CarrierCode", "AA");
Issue.Add("TravelAgentCode", "32165464");
Issue.Add("TravelAgentName", "Washington Hilton");
Issue.Add("Date", "2017-01-10");
Issue.Add("Country", "ARG");
Issue.Add("City", "Buenos Aires");
Issue.Add("Address", "Av. Rivadavia 1111");

Ticket.Add("Issue", Issue);
Ticket.Add("TotalFareAmount", "80000");
Ticket.Add("TotalTaxAmount", "25200");
Ticket.Add("TotalFeeAmount", "14800");

pspAirlineDetails.Add("Ticket", Ticket);

data.Add("psp_AirlineDetails", pspAirlineDetails);
