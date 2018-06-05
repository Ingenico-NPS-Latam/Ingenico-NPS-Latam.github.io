import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.createPaymentMethodFromPayment(data);

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
cardOutputDetails.getValue("IIN");
cardOutputDetails.getValue("Last4");
cardOutputDetails.getValue("NumberLength");
cardOutputDetails.getValue("MaskedNumber");
cardOutputDetails.getValue("MaskedNumberAlternative");

pspPaymentMethod.getValue("FingerPrint");
pspPaymentMethod.getValue("CreatedAt");
pspPaymentMethod.getValue("UpdatedAt");

response.getValue("psp_CustomerId");
response.getValue("psp_PosDateTime");
