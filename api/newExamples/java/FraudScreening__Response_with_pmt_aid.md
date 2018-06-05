import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.fraudScreening(data);

response.getValue("psp_ResponseCod");
response.getValue("psp_ResponseMsg");

ComplexElement pspResult = response.getComplexElement("psp_Result");
pspResult.getValue("ResultCode");
pspResult.getValue("ResultDescription");

response.getValue("psp_OrderId");
response.getValue("psp_MerchantId");
response.getValue("psp_MerchTxRef");
response.getValue("psp_MerchOrderId");
response.getValue("psp_Amount");
response.getValue("psp_NumPayments");
response.getValue("psp_Currency");
response.getValue("psp_Country");
response.getValue("psp_Product");
response.getValue("psp_PosDateTime");
response.getValue("psp_CreatedAt");
