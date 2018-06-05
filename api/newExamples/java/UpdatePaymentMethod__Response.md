import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.updatePaymentMethod(data);

response.getValue("psp_ResponseCod");
response.getValue("psp_ResponseMsg");
response.getValue("psp_MerchantId");

ComplexElement pspPaymentMethod = response.getComplexElement("psp_PaymentMethod");
pspPaymentMethod.getValue("PaymentMethodId");
pspPaymentMethod.getValue("PaymentMethodTag");
pspPaymentMethod.getValue("Product");

ComplexElement cardOutputDetails = psp_PaymentMethod.getComplexElement("CardOutputDetails");
cardOutputDetails.getValue("ExpirationDate");
cardOutputDetails.getValue("ExpirationYear");
cardOutputDetails.getValue("ExpirationMonth");
cardOutputDetails.getValue("HolderName");
cardOutputDetails.getValue("IIN");
cardOutputDetails.getValue("Last4");
cardOutputDetails.getValue("NumberLength");
cardOutputDetails.getValue("MaskedNumber");
cardOutputDetails.getValue("MaskedNumberAlternative");

pspPaymentMethod.getValue("FingerPrint");

ComplexElement person = psp_PaymentMethod.getComplexElement("Person");
person.getValue("FirstName");
person.getValue("LastName");
person.getValue("MiddleName");
person.getValue("PhoneNumber1");
person.getValue("PhoneNumber2");
person.getValue("Gender");
person.getValue("DateOfBirth");
person.getValue("Nationality");
person.getValue("IDNumber");
person.getValue("IDType");


ComplexElement address = psp_PaymentMethod.getComplexElement("Address");
address.getValue("Street");
address.getValue("HouseNumber");
address.getValue("AdditionalInfo");
address.getValue("City");
address.getValue("StateProvince");
address.getValue("Country");
address.getValue("ZipCode");

pspPaymentMethod.getValue("CreatedAt");
pspPaymentMethod.getValue("UpdatedAt");

response.getValue("psp_PosDateTime");
