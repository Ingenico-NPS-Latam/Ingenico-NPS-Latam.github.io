RootElement data = new RootElement();


ComplexElement MerchantDetails = new ComplexElement();
MerchantDetails.Add("Type", "2 A");

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

MerchantDetails.Add("SellerDetails", SellerDetails);

data.Add("MerchantDetails", MerchantDetails);
