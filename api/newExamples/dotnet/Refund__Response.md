using System;
using NpsSDK;

RootElement response = npsSdk.Refund(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_ResponseExtended");
response.GetValue("psp_TransactionId");
response.GetValue("psp_TransactionId_Orig");
response.GetValue("psp_MerchantId");
response.GetValue("psp_MerchTxRef");
response.GetValue("psp_MerchOrderId");
response.GetValue("psp_RefundedAmount");
response.GetValue("psp_CapturedAmount_Orig");
response.GetValue("psp_AuthorizationCode");
response.GetValue("psp_BatchNro");
response.GetValue("psp_TicketNumber");
response.GetValue("psp_Product");
response.GetValue("psp_ClExternalMerchant");
response.GetValue("psp_ClExternalTerminal");
response.GetValue("psp_ClResponseCod");
response.GetValue("psp_ClResponseMsg");
response.GetValue("psp_PosDateTime");
response.GetValue("psp_CreatedAt");
