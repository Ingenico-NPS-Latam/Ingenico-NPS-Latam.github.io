RootElement data = new RootElement();

data.Add("psp_MerchantId", "sdk_test");
data.Add("psp_MerchTxRef", "ORDER1000-1");
data.Add("psp_MerchAdditionalRef", "ADDITIONAL-REF1234");
data.Add("psp_Product", "14");
data.Add("psp_CardNumber", "4507990000000010");
data.Add("psp_CardExpirationDate", "2501");
data.Add("psp_CardSecurityCode", "321");
data.Add("psp_CardHolderName", "JOHN DOE");
data.Add("psp_PaymentAmount", "10050");
data.Add("psp_Amount", "15050");
data.Add("psp_NumPayments", "1");
data.Add("psp_SoftDescriptor", "Compra Art 15");

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

ComplexElement pspVaultReference = new ComplexElement();
pspVaultReference.Add("PaymentMethodId", "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE");
pspVaultReference.Add("CustomerId", "K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f");

data.Add("psp_VaultReference", pspVaultReference);
