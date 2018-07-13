RootElement data = new RootElement();


ComplexElement ShippingDetails = new ComplexElement();
ShippingDetails.add("TrackingNumber", "154DDD54DWW11");
ShippingDetails.add("Method", "1");
ShippingDetails.add("Carrier", "200");
ShippingDetails.add("DeliveryDate", "2014-11-20");
ShippingDetails.add("FreightAmount", "15000");
ShippingDetails.add("GiftMessage", "Happy Birthday!");
ShippingDetails.add("GiftWrapping", "1");

ComplexElement PrimaryRecipient = new ComplexElement();
PrimaryRecipient.add("DateOfBirth", "1979-01-12");
PrimaryRecipient.add("FirstName", "John");
PrimaryRecipient.add("Gender", "M");
PrimaryRecipient.add("IDNumber", "54111111");
PrimaryRecipient.add("IDType", "200");
PrimaryRecipient.add("LastName", "Doe");
PrimaryRecipient.add("MiddleName", "Michael");
PrimaryRecipient.add("Nationality", "ARG");
PrimaryRecipient.add("PhoneNumber1", "+1 011 11111111");
PrimaryRecipient.add("PhoneNumber2", "+1 011 22222222");

ShippingDetails.add("PrimaryRecipient", PrimaryRecipient);

ComplexElement SecondaryRecipient = new ComplexElement();
SecondaryRecipient.add("DateOfBirth", "1979-01-12");
SecondaryRecipient.add("FirstName", "John");
SecondaryRecipient.add("Gender", "M");
SecondaryRecipient.add("IDNumber", "54111111");
SecondaryRecipient.add("IDType", "200");
SecondaryRecipient.add("LastName", "Doe");
SecondaryRecipient.add("MiddleName", "Michael");
SecondaryRecipient.add("Nationality", "ARG");
SecondaryRecipient.add("PhoneNumber1", "+1 011 11111111");
SecondaryRecipient.add("PhoneNumber2", "+1 011 22222222");

ShippingDetails.add("SecondaryRecipient", SecondaryRecipient);

ComplexElement Address = new ComplexElement();
Address.add("AdditionalInfo", "2 A");
Address.add("City", "Miami");
Address.add("Country", "USA");
Address.add("HouseNumber", "1245");
Address.add("StateProvince", "Florida");
Address.add("Street", "Av. Collins");
Address.add("ZipCode", "33140");

ShippingDetails.add("Address", Address);

data.add("ShippingDetails", ShippingDetails);
