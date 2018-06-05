ComplexElement merchantDetails = response.getComplexElement("MerchantDetails");


merchantDetails := merchantDetails.MerchantDetails
fmt.Printf(merchantDetails.Type)

sellerDetails := MerchantDetails.SellerDetails
fmt.Printf(sellerDetails.IDNumber)
fmt.Printf(sellerDetails.IDType)
fmt.Printf(sellerDetails.Name)
fmt.Printf(sellerDetails.Invoice)
fmt.Printf(sellerDetails.PurchaseDescription)

address := SellerDetails.Address
fmt.Printf(address.AdditionalInfo)
fmt.Printf(address.City)
fmt.Printf(address.Country)
fmt.Printf(address.HouseNumber)
fmt.Printf(address.StateProvince)
fmt.Printf(address.Street)
fmt.Printf(address.ZipCode)

fmt.Printf(sellerDetails.MCC)
fmt.Printf(sellerDetails.ChannelCode)
fmt.Printf(sellerDetails.GeoCode)


