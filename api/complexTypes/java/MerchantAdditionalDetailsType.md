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