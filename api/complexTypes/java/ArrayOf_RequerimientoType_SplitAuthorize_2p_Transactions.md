RootElement data = new RootElement();

data.add("psp_MerchantId", "sdk_test");
data.add("psp_MerchTxRef", "ORDER1000-1");
data.add("psp_MerchAdditionalRef", "ADDITIONAL-REF1234");
data.add("psp_Product", "14");
data.add("psp_CardNumber", "4507990000000010");
data.add("psp_CardExpirationDate", "2501");
data.add("psp_CardSecurityCode", "321");
data.add("psp_CardHolderName", "JOHN DOE");
data.add("psp_PaymentAmount", "10050");
data.add("psp_Amount", "15050");
data.add("psp_NumPayments", "1");
data.add("psp_SoftDescriptor", "Compra Art 15");

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

ComplexElement pspVaultReference = new ComplexElement();
pspVaultReference.add("PaymentMethodId", "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE");
pspVaultReference.add("CustomerId", "K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f");

data.add("psp_VaultReference", pspVaultReference);
