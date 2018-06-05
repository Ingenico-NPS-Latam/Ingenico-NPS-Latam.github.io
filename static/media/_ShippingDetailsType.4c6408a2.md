ComplexElement shippingDetails = response.getComplexElement("ShippingDetails");


local shippingDetails = shippingDetails.ShippingDetails
print(shippingDetails.TrackingNumber)
print(shippingDetails.Method)
print(shippingDetails.Carrier)
print(shippingDetails.DeliveryDate)
print(shippingDetails.FreightAmount)
print(shippingDetails.GiftMessage)
print(shippingDetails.GiftWrapping)

local primaryRecipient = ShippingDetails.PrimaryRecipient
print(primaryRecipient.DateOfBirth)
print(primaryRecipient.FirstName)
print(primaryRecipient.Gender)
print(primaryRecipient.IDNumber)
print(primaryRecipient.IDType)
print(primaryRecipient.LastName)
print(primaryRecipient.MiddleName)
print(primaryRecipient.Nationality)
print(primaryRecipient.PhoneNumber1)
print(primaryRecipient.PhoneNumber2)


local secondaryRecipient = ShippingDetails.SecondaryRecipient
print(secondaryRecipient.DateOfBirth)
print(secondaryRecipient.FirstName)
print(secondaryRecipient.Gender)
print(secondaryRecipient.IDNumber)
print(secondaryRecipient.IDType)
print(secondaryRecipient.LastName)
print(secondaryRecipient.MiddleName)
print(secondaryRecipient.Nationality)
print(secondaryRecipient.PhoneNumber1)
print(secondaryRecipient.PhoneNumber2)


local address = ShippingDetails.Address
print(address.AdditionalInfo)
print(address.City)
print(address.Country)
print(address.HouseNumber)
print(address.StateProvince)
print(address.Street)
print(address.ZipCode)


