import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement paymentMethodInputDetails = response.getComplexElement("PaymentMethodInputDetails");


ComplexElement pspPaymentMethodInputDetails = paymentMethodInputDetails.getComplexElement("psp_PaymentMethodInputDetails");
pspPaymentMethodInputDetails.getValue("PaymentMethodToken");
pspPaymentMethodInputDetails.getValue("PaymentMethodTag");

ComplexElement cardInputDetails = psp_PaymentMethodInputDetails.getComplexElement("CardInputDetails");
cardInputDetails.getValue("Number");
cardInputDetails.getValue("ExpirationDate");
cardInputDetails.getValue("SecurityCode");
cardInputDetails.getValue("HolderName");


ComplexElement person = psp_PaymentMethodInputDetails.getComplexElement("Person");
person.getValue("DateOfBirth");
person.getValue("FirstName");
person.getValue("Gender");
person.getValue("IDNumber");
person.getValue("IDType");
person.getValue("LastName");
person.getValue("MiddleName");
person.getValue("Nationality");
person.getValue("PhoneNumber1");
person.getValue("PhoneNumber2");


ComplexElement address = psp_PaymentMethodInputDetails.getComplexElement("Address");
address.getValue("AdditionalInfo");
address.getValue("City");
address.getValue("Country");
address.getValue("HouseNumber");
address.getValue("StateProvince");
address.getValue("Street");
address.getValue("ZipCode");


