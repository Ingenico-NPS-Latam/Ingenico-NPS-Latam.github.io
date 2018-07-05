using System;
using NpsSDK;

ComplexElement MerchantDetails = response.GetComplexElement("MerchantDetails");


ComplexElement merchantDetails = MerchantDetails.GetComplexElement("MerchantDetails");
merchantDetails.GetValue("Type");

ComplexElement sellerDetails = MerchantDetails.GetComplexElement("SellerDetails");
sellerDetails.GetValue("IDNumber");
sellerDetails.GetValue("IDType");
sellerDetails.GetValue("Name");
sellerDetails.GetValue("Invoice");
sellerDetails.GetValue("PurchaseDescription");

ComplexElement address = SellerDetails.GetComplexElement("Address");
address.GetValue("AdditionalInfo");
address.GetValue("City");
address.GetValue("Country");
address.GetValue("HouseNumber");
address.GetValue("StateProvince");
address.GetValue("Street");
address.GetValue("ZipCode");

sellerDetails.GetValue("MCC");
sellerDetails.GetValue("ChannelCode");
sellerDetails.GetValue("GeoCode");


