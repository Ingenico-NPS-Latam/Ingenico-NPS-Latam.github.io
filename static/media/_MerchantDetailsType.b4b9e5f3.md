ComplexElement merchantDetails = response.getComplexElement("MerchantDetails");


local merchantDetails = merchantDetails.MerchantDetails
print(merchantDetails.Type)

local sellerDetails = MerchantDetails.SellerDetails
print(sellerDetails.IDNumber)
print(sellerDetails.IDType)
print(sellerDetails.Name)
print(sellerDetails.Invoice)
print(sellerDetails.PurchaseDescription)

local address = SellerDetails.Address
print(address.AdditionalInfo)
print(address.City)
print(address.Country)
print(address.HouseNumber)
print(address.StateProvince)
print(address.Street)
print(address.ZipCode)

print(sellerDetails.MCC)
print(sellerDetails.ChannelCode)
print(sellerDetails.GeoCode)


