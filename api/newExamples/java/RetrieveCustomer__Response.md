import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.retrieveCustomer(data);

response.getValue("psp_ResponseCod");
response.getValue("psp_ResponseMsg");
response.getValue("psp_MerchantId");
response.getValue("psp_CustomerId");
response.getValue("psp_EmailAddress");
response.getValue("psp_AlternativeEmailAddress");
response.getValue("psp_AccountID");
response.getValue("psp_AccountCreatedAt");
response.getValue("psp_PosDateTime");
