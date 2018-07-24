import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement sellerDetails = response.getComplexElement("SellerDetails");


ComplexElement sellerDetails = sellerDetails.getComplexElement("SellerDetails");
sellerDetails.getValue("IDNumber");
sellerDetails.getValue("IDType");
sellerDetails.getValue("Name");
sellerDetails.getValue("Invoice");
sellerDetails.getValue("PurchaseDescription");

ComplexElement address = SellerDetails.getComplexElement("Address");
address.getValue("AdditionalInfo");
address.getValue("City");
address.getValue("Country");
address.getValue("HouseNumber");
address.getValue("StateProvince");
address.getValue("Street");
address.getValue("ZipCode");

sellerDetails.getValue("MCC");
sellerDetails.getValue("ChannelCode");
sellerDetails.getValue("GeoCode");
