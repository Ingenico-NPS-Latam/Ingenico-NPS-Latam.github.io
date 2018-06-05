using System;
using NpsSDK;

RootElement response = npsSdk.QueryCardDetails(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_MerchantId");
response.GetValue("psp_QueryCriteria");
response.GetValue("psp_QueryCriteriaId");
response.GetValue("psp_PosDateTime");

ComplexElement pspCardOutputDetails = response.GetComplexElement("psp_CardOutputDetails");
pspCardOutputDetails.GetValue("Number");
pspCardOutputDetails.GetValue("ExpirationDate");
pspCardOutputDetails.GetValue("ExpirationYear");
pspCardOutputDetails.GetValue("ExpirationMonth");
pspCardOutputDetails.GetValue("HolderName");
pspCardOutputDetails.GetValue("IIN");
pspCardOutputDetails.GetValue("Last4");
pspCardOutputDetails.GetValue("NumberLength");
pspCardOutputDetails.GetValue("MaskedNumber");
pspCardOutputDetails.GetValue("MaskedNumberAlternative");

