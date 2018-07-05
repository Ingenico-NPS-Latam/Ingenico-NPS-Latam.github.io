ComplexElement shippingDetails = response.getComplexElement("ShippingDetails");


shippingDetails := shippingDetails.ShippingDetails
fmt.Printf(shippingDetails.TrackingNumber)
fmt.Printf(shippingDetails.Method)
fmt.Printf(shippingDetails.Carrier)
fmt.Printf(shippingDetails.DeliveryDate)
fmt.Printf(shippingDetails.FreightAmount)
fmt.Printf(shippingDetails.GiftMessage)
fmt.Printf(shippingDetails.GiftWrapping)

primaryRecipient := ShippingDetails.PrimaryRecipient
fmt.Printf(primaryRecipient.DateOfBirth)
fmt.Printf(primaryRecipient.FirstName)
fmt.Printf(primaryRecipient.Gender)
fmt.Printf(primaryRecipient.IDNumber)
fmt.Printf(primaryRecipient.IDType)
fmt.Printf(primaryRecipient.LastName)
fmt.Printf(primaryRecipient.MiddleName)
fmt.Printf(primaryRecipient.Nationality)
fmt.Printf(primaryRecipient.PhoneNumber1)
fmt.Printf(primaryRecipient.PhoneNumber2)


secondaryRecipient := ShippingDetails.SecondaryRecipient
fmt.Printf(secondaryRecipient.DateOfBirth)
fmt.Printf(secondaryRecipient.FirstName)
fmt.Printf(secondaryRecipient.Gender)
fmt.Printf(secondaryRecipient.IDNumber)
fmt.Printf(secondaryRecipient.IDType)
fmt.Printf(secondaryRecipient.LastName)
fmt.Printf(secondaryRecipient.MiddleName)
fmt.Printf(secondaryRecipient.Nationality)
fmt.Printf(secondaryRecipient.PhoneNumber1)
fmt.Printf(secondaryRecipient.PhoneNumber2)


address := ShippingDetails.Address
fmt.Printf(address.AdditionalInfo)
fmt.Printf(address.City)
fmt.Printf(address.Country)
fmt.Printf(address.HouseNumber)
fmt.Printf(address.StateProvince)
fmt.Printf(address.Street)
fmt.Printf(address.ZipCode)


