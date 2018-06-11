import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.queryCardDetails(data);

response.getValue("psp_ResponseCod");
response.getValue("psp_ResponseMsg");
response.getValue("psp_MerchantId");
response.getValue("psp_QueryCriteria");
response.getValue("psp_QueryCriteriaId");
response.getValue("psp_PosDateTime");

ComplexElement pspCardOutputDetails = response.getComplexElement("psp_CardOutputDetails");
pspCardOutputDetails.getValue("Number");
pspCardOutputDetails.getValue("ExpirationDate");
pspCardOutputDetails.getValue("ExpirationYear");
pspCardOutputDetails.getValue("ExpirationMonth");
pspCardOutputDetails.getValue("HolderName");
pspCardOutputDetails.getValue("IIN");
pspCardOutputDetails.getValue("Last4");
pspCardOutputDetails.getValue("NumberLength");
pspCardOutputDetails.getValue("MaskedNumber");
pspCardOutputDetails.getValue("MaskedNumberAlternative");

