import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.notifyFraudScreeningReview(data);

response.getValue("psp_ResponseCod");
response.getValue("psp_ResponseMsg");
response.getValue("psp_MerchantId");
response.getValue("psp_PosDateTime");
