import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.createPaymentMethodToken(data);

response.getValue("psp_ResponseCod");
response.getValue("psp_ResponseMsg");
response.getValue("psp_MerchantId");
response.getValue("psp_PaymentMethodToken");
response.getValue("psp_Product");

ComplexElement pspWalletOutputDetails = response.getComplexElement("psp_WalletOutputDetails");

ComplexElement cardOutputDetails = psp_WalletOutputDetails.getComplexElement("CardOutputDetails");
cardOutputDetails.getValue("ExpirationDate");
cardOutputDetails.getValue("ExpirationYear");
cardOutputDetails.getValue("ExpirationMonth");
cardOutputDetails.getValue("HolderName");
cardOutputDetails.getValue("IIN");
cardOutputDetails.getValue("Last4");
cardOutputDetails.getValue("NumberLength");
cardOutputDetails.getValue("MaskedNumber");
cardOutputDetails.getValue("MaskedNumberAlternative");


ComplexElement shippingDetails = psp_WalletOutputDetails.getComplexElement("ShippingDetails");
shippingDetails.getValue("Method");

ComplexElement primaryRecipient = ShippingDetails.getComplexElement("PrimaryRecipient");
primaryRecipient.getValue("FirstName");
primaryRecipient.getValue("PhoneNumber1");


ComplexElement address = ShippingDetails.getComplexElement("Address");
address.getValue("Street");

ComplexElement houseNumber = Address.getComplexElement("HouseNumber");

address.getValue("AdditionalInfo");
address.getValue("City");
address.getValue("Country");
address.getValue("ZipCode");




ComplexElement pspAddress = response.getComplexElement("psp_Address");
pspAddress.getValue("Street");
pspAddress.getValue("AdditionalInfo");
pspAddress.getValue("City");
pspAddress.getValue("Country");
pspAddress.getValue("ZipCode");

response.getValue("psp_AlreadyUsed");
response.getValue("psp_CreatedAt");
response.getValue("psp_UpdatedAt");
