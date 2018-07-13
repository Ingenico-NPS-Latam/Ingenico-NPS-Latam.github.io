RootElement data = new RootElement();

data.add("psp_ResponseCod", "2");
data.add("psp_ResponseMsg", "Transaccion exitosa - Aprobada");
data.add("psp_ResponseExtended", "Aprobada");
data.add("psp_TransactionId", "100022");
data.add("psp_MerchantId", "sdk_test");
data.add("psp_TxSource", "WEB");
data.add("psp_Operation", "TC  Autorizacion");
data.add("psp_MerchTxRef", "ORDER1000-1");
data.add("psp_MerchOrderId", "ORDER1000");
data.add("psp_MerchAdditionalRef", "ADDITIONAL-REF1234");
data.add("psp_Amount", "15050");
data.add("psp_NumPayments", "1");
data.add("psp_PaymentAmount", "10050");
data.add("psp_Currency", "032");
data.add("psp_Country", "ARG");
data.add("psp_Product", "14");
data.add("psp_AuthorizationCode", "352123");
data.add("psp_BatchNro", "1254");
data.add("psp_SequenceNumber", "64564321654");
data.add("psp_TicketNumber", "1254");
data.add("psp_CardNumber_FSD", "125478");
data.add("psp_CardNumber_LFD", "0001");
data.add("psp_CardMask", "451423XXXXXX1452");
data.add("psp_CardHolderName", "JOHN DOE");
data.add("psp_CustomerMail", "client@client.com.ar");
data.add("psp_CustomerId", "P123765");
data.add("psp_CustomerHttpUserAgent", " Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0");
data.add("psp_CustomerIpAddress", "200.123.123.100");
data.add("psp_MerchantMail", "merchant@merchant.com.ar");
data.add("psp_ClTrnId", "365258");
data.add("psp_ClExternalMerchant", "96878987");
data.add("psp_ClExternalTerminal", "14587986");
data.add("psp_ClResponseCod", "155");
data.add("psp_ClResponseMsg", "33140");
data.add("psp_PosDateTime", "2008-01-12 13:05:00");
data.add("psp_PurchaseDescription", "Com. X Art 1555");
data.add("psp_SoftDescriptor", "Compra Art 15");
data.add("psp_Plan", "PlanZ");
data.add("psp_3dSecure_XID", "MjY0MjAxNjA4MDIyMDUzMzYyNjU=");
data.add("psp_3dSecure_CAVV", "AAABBYZ3N5Qhl3kBU3c3ELGUsMY=");
data.add("psp_3dSecure_Eci", "05");
data.add("psp_3dSecure_EciMsg", "");
data.add("psp_3dSecure_Secured", "1");
data.add("psp_CreatedAt", "2008-01-12 13:05:35-03:00");

ComplexElement pspAmountAdditionalDetails = new ComplexElement();
pspAmountAdditionalDetails.add("Tip", "20000");
pspAmountAdditionalDetails.add("Discount", "11000");

ComplexElementArray Taxes = new ComplexElementArray();

ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
Taxes1.add("TypeId", "500");
Taxes1.add("Amount", "10000");
Taxes1.add("Rate", "2100");
Taxes1.add("BaseAmount", "10000");

Taxes.add(Taxes1);

ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
Taxes2.add("TypeId", "500");
Taxes2.add("Amount", "10000");
Taxes2.add("Rate", "2100");
Taxes2.add("BaseAmount", "10000");

Taxes.add(Taxes2);

pspAmountAdditionalDetails.add("Taxes", Taxes);

data.add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);

ComplexElement pspFraudScreeningResult = new ComplexElement();
pspFraudScreeningResult.add("ResultCode", "A");
pspFraudScreeningResult.add("ResultDescription", "ACCEPT");
pspFraudScreeningResult.add("AdditionalInfo", "Information");

data.add("psp_FraudScreeningResult", pspFraudScreeningResult);

ComplexElement pspVerificationServicesResult = new ComplexElement();
pspVerificationServicesResult.add("ResultCodeCardSecurityCode", "M");
pspVerificationServicesResult.add("ResultCodeBillingAddress", "M");
pspVerificationServicesResult.add("ResultCodeBillingAddressZipCode", "M");
pspVerificationServicesResult.add("ResultCodeBillingPersonIDType", "M");
pspVerificationServicesResult.add("ResultCodeBillingPersonIDNumber", "M");
pspVerificationServicesResult.add("ResultCodeBillingPersonDateOfBirth", "M");
pspVerificationServicesResult.add("ResultCodeBillingPersonName", "M");
pspVerificationServicesResult.add("ResultCodeBillingPersonPhoneNumber1", "M");
pspVerificationServicesResult.add("ResultCodeCustomerEmailAddress", "M");

data.add("psp_VerificationServicesResult", pspVerificationServicesResult);

ComplexElement pspMerchantAdditionalDetails = new ComplexElement();
pspMerchantAdditionalDetails.add("Type", "2 A");

ComplexElement SellerDetails = new ComplexElement();
SellerDetails.add("IDNumber", "30706033471");
SellerDetails.add("IDType", "205");
SellerDetails.add("Name", "Company S.A.");
SellerDetails.add("Invoice", "54877555");
SellerDetails.add("PurchaseDescription", "Samsung 4K SUHD TV");

ComplexElement Address = new ComplexElement();
Address.add("AdditionalInfo", "2 A");
Address.add("City", "Miami");
Address.add("Country", "USA");
Address.add("HouseNumber", "1245");
Address.add("StateProvince", "Florida");
Address.add("Street", "Av. Collins");
Address.add("ZipCode", "33140");

SellerDetails.add("Address", Address);
SellerDetails.add("MCC", "5732");
SellerDetails.add("ChannelCode", "");
SellerDetails.add("GeoCode", "");

pspMerchantAdditionalDetails.add("SellerDetails", SellerDetails);

data.add("psp_MerchantAdditionalDetails", pspMerchantAdditionalDetails);

ComplexElement pspCustomerAdditionalDetails = new ComplexElement();
pspCustomerAdditionalDetails.add("EmailAddress", "jdoe@email.com");
pspCustomerAdditionalDetails.add("AlternativeEmailAddress", "Jdoe79@email.com");
pspCustomerAdditionalDetails.add("IPAddress", "192.168.158.190");
pspCustomerAdditionalDetails.add("AccountID", "Jdoe78");
pspCustomerAdditionalDetails.add("AccountCreatedAt", "2010-10-23");
pspCustomerAdditionalDetails.add("AccountPreviousActivity", "1");
pspCustomerAdditionalDetails.add("AccountHasCredentials", "1");
pspCustomerAdditionalDetails.add("DeviceType", "1");
pspCustomerAdditionalDetails.add("DeviceFingerPrint", "KJhKHKJgh7777kgh");
pspCustomerAdditionalDetails.add("BrowserLanguage", "ES");
pspCustomerAdditionalDetails.add("HttpUserAgent", "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0");

data.add("psp_CustomerAdditionalDetails", pspCustomerAdditionalDetails);

ComplexElement pspBillingDetails = new ComplexElement();
pspBillingDetails.add("Invoice", "54877555");
pspBillingDetails.add("InvoiceDate", "2017-10-23");
pspBillingDetails.add("InvoiceAmount", "15050");
pspBillingDetails.add("InvoiceCurrency", "032");

ComplexElement Person = new ComplexElement();
Person.add("DateOfBirth", "1979-01-12");
Person.add("FirstName", "John");
Person.add("Gender", "M");
Person.add("IDNumber", "54111111");
Person.add("IDType", "200");
Person.add("LastName", "Doe");
Person.add("MiddleName", "Michael");
Person.add("Nationality", "ARG");
Person.add("PhoneNumber1", "+1 011 11111111");
Person.add("PhoneNumber2", "+1 011 22222222");

pspBillingDetails.add("Person", Person);

ComplexElement Address = new ComplexElement();
Address.add("AdditionalInfo", "2 A");
Address.add("City", "Miami");
Address.add("Country", "USA");
Address.add("HouseNumber", "1245");
Address.add("StateProvince", "Florida");
Address.add("Street", "Av. Collins");
Address.add("ZipCode", "33140");

pspBillingDetails.add("Address", Address);

data.add("psp_BillingDetails", pspBillingDetails);

ComplexElement pspShippingDetails = new ComplexElement();
pspShippingDetails.add("TrackingNumber", "154DDD54DWW11");
pspShippingDetails.add("Method", "1");
pspShippingDetails.add("Carrier", "200");
pspShippingDetails.add("DeliveryDate", "2014-11-20");
pspShippingDetails.add("FreightAmount", "15000");
pspShippingDetails.add("GiftMessage", "Happy Birthday!");
pspShippingDetails.add("GiftWrapping", "1");

ComplexElement PrimaryRecipient = new ComplexElement();
PrimaryRecipient.add("DateOfBirth", "1979-01-12");
PrimaryRecipient.add("FirstName", "John");
PrimaryRecipient.add("Gender", "M");
PrimaryRecipient.add("IDNumber", "54111111");
PrimaryRecipient.add("IDType", "200");
PrimaryRecipient.add("LastName", "Doe");
PrimaryRecipient.add("MiddleName", "Michael");
PrimaryRecipient.add("Nationality", "ARG");
PrimaryRecipient.add("PhoneNumber1", "+1 011 11111111");
PrimaryRecipient.add("PhoneNumber2", "+1 011 22222222");

pspShippingDetails.add("PrimaryRecipient", PrimaryRecipient);

ComplexElement SecondaryRecipient = new ComplexElement();
SecondaryRecipient.add("DateOfBirth", "1979-01-12");
SecondaryRecipient.add("FirstName", "John");
SecondaryRecipient.add("Gender", "M");
SecondaryRecipient.add("IDNumber", "54111111");
SecondaryRecipient.add("IDType", "200");
SecondaryRecipient.add("LastName", "Doe");
SecondaryRecipient.add("MiddleName", "Michael");
SecondaryRecipient.add("Nationality", "ARG");
SecondaryRecipient.add("PhoneNumber1", "+1 011 11111111");
SecondaryRecipient.add("PhoneNumber2", "+1 011 22222222");

pspShippingDetails.add("SecondaryRecipient", SecondaryRecipient);

ComplexElement Address = new ComplexElement();
Address.add("AdditionalInfo", "2 A");
Address.add("City", "Miami");
Address.add("Country", "USA");
Address.add("HouseNumber", "1245");
Address.add("StateProvince", "Florida");
Address.add("Street", "Av. Collins");
Address.add("ZipCode", "33140");

pspShippingDetails.add("Address", Address);

data.add("psp_ShippingDetails", pspShippingDetails);

ComplexElementArray pspOrderDetails = new ComplexElementArray();

ComplexElementArrayItem pspOrderDetails1 = new ComplexElementArrayItem();
pspOrderDetails1.add("Quantity", "10");
pspOrderDetails1.add("UnitPrice", "10050");
pspOrderDetails1.add("Description", "Blue pencil");
pspOrderDetails1.add("Type", "1002");
pspOrderDetails1.add("SkuCode", "SO-4587885545");
pspOrderDetails1.add("ManufacturerPartNumber", "CN-0N2828421-3AD-02CD");
pspOrderDetails1.add("Risk", "H");

pspOrderDetails.add(pspOrderDetails1);

ComplexElementArrayItem pspOrderDetails2 = new ComplexElementArrayItem();
pspOrderDetails2.add("Quantity", "10");
pspOrderDetails2.add("UnitPrice", "10050");
pspOrderDetails2.add("Description", "Blue pencil");
pspOrderDetails2.add("Type", "1002");
pspOrderDetails2.add("SkuCode", "SO-4587885545");
pspOrderDetails2.add("ManufacturerPartNumber", "CN-0N2828421-3AD-02CD");
pspOrderDetails2.add("Risk", "H");

pspOrderDetails.add(pspOrderDetails2);

data.add("psp_OrderDetails", pspOrderDetails);

ComplexElement pspAirlineDetails = new ComplexElement();
pspAirlineDetails.add("PNR", "154DDD54DWW11");

ComplexElementArray Legs = new ComplexElementArray();

ComplexElementArrayItem Legs1 = new ComplexElementArrayItem();
Legs1.add("DepartureAirport", "EZE");
Legs1.add("DepartureDatetime", "2014-05-12 13:05:00");
Legs1.add("DepartureAirportTimezone", "-03:00");
Legs1.add("ArrivalAirport", "AMS");
Legs1.add("CarrierCode", "KL");
Legs1.add("FlightNumber", "842");
Legs1.add("FareBasisCode", "HL7LNR");
Legs1.add("FareClassCode", "FR");
Legs1.add("BaseFare", "30000");
Legs1.add("BaseFareCurrency", "032");

Legs.add(Legs1);

pspAirlineDetails.add("Legs", Legs);

ComplexElementArray Passengers = new ComplexElementArray();

ComplexElementArrayItem Passengers1 = new ComplexElementArrayItem();
Passengers1.add("FirstName", "John");
Passengers1.add("LastName", "Doe");
Passengers1.add("MiddleName", "Michael");
Passengers1.add("Type", "A");
Passengers1.add("DateOfBirth", "1979-01-12");
Passengers1.add("Nationality", "ARG");
Passengers1.add("IDNumber", "54111111");
Passengers1.add("IDType", "100");
Passengers1.add("IDCountry", "ARG");
Passengers1.add("LoyaltyNumber", "254587547");
Passengers1.add("LoyaltyTier", "1");

Passengers.add(Passengers1);

pspAirlineDetails.add("Passengers", Passengers);

ComplexElement Ticket = new ComplexElement();
Ticket.add("TicketNumber", "07411865255578");
Ticket.add("Eticket", "1");
Ticket.add("Restricted", "1");

ComplexElement Issue = new ComplexElement();
Issue.add("CarrierCode", "AA");
Issue.add("TravelAgentCode", "32165464");
Issue.add("TravelAgentName", "Washington Hilton");
Issue.add("Date", "2017-01-10");
Issue.add("Country", "ARG");
Issue.add("City", "Buenos Aires");
Issue.add("Address", "Av. Rivadavia 1111");

Ticket.add("Issue", Issue);
Ticket.add("TotalFareAmount", "80000");
Ticket.add("TotalTaxAmount", "25200");
Ticket.add("TotalFeeAmount", "14800");

pspAirlineDetails.add("Ticket", Ticket);

data.add("psp_AirlineDetails", pspAirlineDetails);
