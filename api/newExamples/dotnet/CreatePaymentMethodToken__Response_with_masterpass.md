using System;
using NpsSDK;

RootElement response = npsSdk.CreatePaymentMethodToken(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_MerchantId");
response.GetValue("psp_PaymentMethodToken");
response.GetValue("psp_Product");

ComplexElement pspWalletOutputDetails = response.GetComplexElement("psp_WalletOutputDetails");

ComplexElement cardOutputDetails = psp_WalletOutputDetails.GetComplexElement("CardOutputDetails");
cardOutputDetails.GetValue("ExpirationDate");
cardOutputDetails.GetValue("ExpirationYear");
cardOutputDetails.GetValue("ExpirationMonth");
cardOutputDetails.GetValue("HolderName");
cardOutputDetails.GetValue("IIN");
cardOutputDetails.GetValue("Last4");
cardOutputDetails.GetValue("NumberLength");
cardOutputDetails.GetValue("MaskedNumber");
cardOutputDetails.GetValue("MaskedNumberAlternative");


ComplexElement shippingDetails = psp_WalletOutputDetails.GetComplexElement("ShippingDetails");
shippingDetails.GetValue("Method");

ComplexElement primaryRecipient = ShippingDetails.GetComplexElement("PrimaryRecipient");
primaryRecipient.GetValue("FirstName");
primaryRecipient.GetValue("PhoneNumber1");


ComplexElement address = ShippingDetails.GetComplexElement("Address");
address.GetValue("Street");

ComplexElement houseNumber = Address.GetComplexElement("HouseNumber");

address.GetValue("AdditionalInfo");
address.GetValue("City");
address.GetValue("Country");
address.GetValue("ZipCode");




ComplexElement pspAddress = response.GetComplexElement("psp_Address");
pspAddress.GetValue("Street");
pspAddress.GetValue("AdditionalInfo");
pspAddress.GetValue("City");
pspAddress.GetValue("Country");
pspAddress.GetValue("ZipCode");

response.GetValue("psp_AlreadyUsed");
response.GetValue("psp_CreatedAt");
response.GetValue("psp_UpdatedAt");
