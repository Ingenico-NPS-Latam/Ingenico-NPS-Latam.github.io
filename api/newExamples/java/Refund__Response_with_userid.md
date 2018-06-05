import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.refund(data);

response.getValue("psp_ResponseCod");
response.getValue("psp_ResponseMsg");
response.getValue("psp_ResponseExtended");
response.getValue("psp_TransactionId");
response.getValue("psp_TransactionId_Orig");
response.getValue("psp_MerchantId");
response.getValue("psp_MerchTxRef");
response.getValue("psp_MerchOrderId");
response.getValue("psp_RefundedAmount");
response.getValue("psp_CapturedAmount_Orig");
response.getValue("psp_AuthorizationCode");
response.getValue("psp_BatchNro");
response.getValue("psp_TicketNumber");
response.getValue("psp_Product");
response.getValue("psp_ClExternalMerchant");
response.getValue("psp_ClExternalTerminal");
response.getValue("psp_ClResponseCod");
response.getValue("psp_ClResponseMsg");
response.getValue("psp_PosDateTime");
response.getValue("psp_CreatedAt");
