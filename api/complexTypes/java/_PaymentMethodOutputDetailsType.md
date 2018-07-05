import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement paymentMethodOutputDetails = response.getComplexElement("PaymentMethodOutputDetails");


ComplexElement pspPaymentMethodOutputDetails = paymentMethodOutputDetails.getComplexElement("psp_PaymentMethodOutputDetails");
pspPaymentMethodOutputDetails.getValue("PaymentMethodId");
pspPaymentMethodOutputDetails.getValue("PaymentMethodTag");
pspPaymentMethodOutputDetails.getValue("Product");

ComplexElement cardOutputDetails = psp_PaymentMethodOutputDetails.getComplexElement("CardOutputDetails");
cardOutputDetails.getValue("ExpirationDate");
cardOutputDetails.getValue("ExpirationYear");
cardOutputDetails.getValue("ExpirationMonth");
cardOutputDetails.getValue("HolderName");
cardOutputDetails.getValue("IIN");
cardOutputDetails.getValue("Last4");
cardOutputDetails.getValue("NumberLength");
cardOutputDetails.getValue("MaskedNumber");
cardOutputDetails.getValue("MaskedNumberAlternative");

pspPaymentMethodOutputDetails.getValue("FingerPrint");

ComplexElement person = psp_PaymentMethodOutputDetails.getComplexElement("Person");
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


ComplexElement address = psp_PaymentMethodOutputDetails.getComplexElement("Address");
address.getValue("AdditionalInfo");
address.getValue("City");
address.getValue("Country");
address.getValue("HouseNumber");
address.getValue("StateProvince");
address.getValue("Street");
address.getValue("ZipCode");

pspPaymentMethodOutputDetails.getValue("CreatedAt");
pspPaymentMethodOutputDetails.getValue("UpdatedAt");

