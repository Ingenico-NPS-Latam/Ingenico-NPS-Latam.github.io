using System;
using NpsSDK;

RootElement response = npsSdk.CreatePaymentMethodFromPayment(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_MerchantId");

ComplexElement pspPaymentMethod = response.GetComplexElement("psp_PaymentMethod");
pspPaymentMethod.GetValue("PaymentMethodId");
pspPaymentMethod.GetValue("PaymentMethodTag");
pspPaymentMethod.GetValue("Product");

ComplexElement cardOutputDetails = psp_PaymentMethod.GetComplexElement("CardOutputDetails");
cardOutputDetails.GetValue("ExpirationDate");
cardOutputDetails.GetValue("ExpirationYear");
cardOutputDetails.GetValue("ExpirationMonth");
cardOutputDetails.GetValue("IIN");
cardOutputDetails.GetValue("Last4");
cardOutputDetails.GetValue("NumberLength");
cardOutputDetails.GetValue("MaskedNumber");
cardOutputDetails.GetValue("MaskedNumberAlternative");

pspPaymentMethod.GetValue("FingerPrint");
pspPaymentMethod.GetValue("CreatedAt");
pspPaymentMethod.GetValue("UpdatedAt");

response.GetValue("psp_PosDateTime");
