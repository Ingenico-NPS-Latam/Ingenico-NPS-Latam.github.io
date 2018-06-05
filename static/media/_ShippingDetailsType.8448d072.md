import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement shippingDetails = response.getComplexElement("ShippingDetails");


ComplexElement shippingDetails = shippingDetails.getComplexElement("ShippingDetails");
shippingDetails.getValue("TrackingNumber");
shippingDetails.getValue("Method");
shippingDetails.getValue("Carrier");
shippingDetails.getValue("DeliveryDate");
shippingDetails.getValue("FreightAmount");
shippingDetails.getValue("GiftMessage");
shippingDetails.getValue("GiftWrapping");

ComplexElement primaryRecipient = ShippingDetails.getComplexElement("PrimaryRecipient");
primaryRecipient.getValue("DateOfBirth");
primaryRecipient.getValue("FirstName");
primaryRecipient.getValue("Gender");
primaryRecipient.getValue("IDNumber");
primaryRecipient.getValue("IDType");
primaryRecipient.getValue("LastName");
primaryRecipient.getValue("MiddleName");
primaryRecipient.getValue("Nationality");
primaryRecipient.getValue("PhoneNumber1");
primaryRecipient.getValue("PhoneNumber2");


ComplexElement secondaryRecipient = ShippingDetails.getComplexElement("SecondaryRecipient");
secondaryRecipient.getValue("DateOfBirth");
secondaryRecipient.getValue("FirstName");
secondaryRecipient.getValue("Gender");
secondaryRecipient.getValue("IDNumber");
secondaryRecipient.getValue("IDType");
secondaryRecipient.getValue("LastName");
secondaryRecipient.getValue("MiddleName");
secondaryRecipient.getValue("Nationality");
secondaryRecipient.getValue("PhoneNumber1");
secondaryRecipient.getValue("PhoneNumber2");


ComplexElement address = ShippingDetails.getComplexElement("Address");
address.getValue("AdditionalInfo");
address.getValue("City");
address.getValue("Country");
address.getValue("HouseNumber");
address.getValue("StateProvince");
address.getValue("Street");
address.getValue("ZipCode");


