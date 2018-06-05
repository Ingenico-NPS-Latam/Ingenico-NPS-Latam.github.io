using System;
using NpsSDK;

RootElement response = npsSdk.CreatePaymentMethodToken(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_MerchantId");
response.GetValue("psp_PaymentMethodToken");
response.GetValue("psp_Product");

ComplexElement pspCardOutputDetails = response.GetComplexElement("psp_CardOutputDetails");
pspCardOutputDetails.GetValue("ExpirationDate");
pspCardOutputDetails.GetValue("ExpirationYear");
pspCardOutputDetails.GetValue("ExpirationMonth");
pspCardOutputDetails.GetValue("HolderName");
pspCardOutputDetails.GetValue("IIN");
pspCardOutputDetails.GetValue("Last4");
pspCardOutputDetails.GetValue("NumberLength");
pspCardOutputDetails.GetValue("MaskedNumber");
pspCardOutputDetails.GetValue("MaskedNumberAlternative");

response.GetValue("psp_AlreadyUsed");
response.GetValue("psp_CreatedAt");
response.GetValue("psp_UpdatedAt");
