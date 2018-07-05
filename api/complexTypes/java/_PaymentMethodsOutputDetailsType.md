import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement paymentMethodsOutputDetails = response.getComplexElement("PaymentMethodsOutputDetails");


ComplexElement pspPaymentMethodsOutputDetails = paymentMethodsOutputDetails.getComplexElement("psp_PaymentMethodsOutputDetails");
pspPaymentMethodsOutputDetails.getValue("PaymentMethodId");
pspPaymentMethodsOutputDetails.getValue("PaymentMethodTag");
pspPaymentMethodsOutputDetails.getValue("Product");

ComplexElement cardOutputDetails = psp_PaymentMethodsOutputDetails.getComplexElement("CardOutputDetails");
cardOutputDetails.getValue("ExpirationDate");
cardOutputDetails.getValue("ExpirationYear");
cardOutputDetails.getValue("ExpirationMonth");
cardOutputDetails.getValue("HolderName");
cardOutputDetails.getValue("IIN");
cardOutputDetails.getValue("Last4");
cardOutputDetails.getValue("MaskedNumber");
cardOutputDetails.getValue("MaskedNumberAlternative");

pspPaymentMethodsOutputDetails.getValue("FingerPrint");

ComplexElement person = psp_PaymentMethodsOutputDetails.getComplexElement("Person");
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


ComplexElement address = psp_PaymentMethodsOutputDetails.getComplexElement("Address");
address.getValue("AdditionalInfo");
address.getValue("City");
address.getValue("Country");
address.getValue("HouseNumber");
address.getValue("StateProvince");
address.getValue("Street");
address.getValue("ZipCode");

pspPaymentMethodsOutputDetails.getValue("CreatedAt");
pspPaymentMethodsOutputDetails.getValue("UpdatedAt");

