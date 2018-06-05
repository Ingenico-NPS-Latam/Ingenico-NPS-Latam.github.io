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

ComplexElement pspCardOutputDetails = response.getComplexElement("psp_CardOutputDetails");
pspCardOutputDetails.getValue("ExpirationDate");
pspCardOutputDetails.getValue("ExpirationYear");
pspCardOutputDetails.getValue("ExpirationMonth");
pspCardOutputDetails.getValue("HolderName");
pspCardOutputDetails.getValue("IIN");
pspCardOutputDetails.getValue("Last4");
pspCardOutputDetails.getValue("NumberLength");
pspCardOutputDetails.getValue("MaskedNumber");
pspCardOutputDetails.getValue("MaskedNumberAlternative");

response.getValue("psp_AlreadyUsed");
response.getValue("psp_CreatedAt");
response.getValue("psp_UpdatedAt");
