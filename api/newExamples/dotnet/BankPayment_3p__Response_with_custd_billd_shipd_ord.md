using System;
using NpsSDK;

RootElement response = npsSdk.BankPayment_3p(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_TransactionId");
response.GetValue("psp_Session3p");
response.GetValue("psp_FrontPSP_URL");
response.GetValue("psp_MerchantId");
response.GetValue("psp_MerchTxRef");
response.GetValue("psp_MerchOrderId");
response.GetValue("psp_Currency");
response.GetValue("psp_Country");
response.GetValue("psp_Product");
response.GetValue("psp_PosDateTime");
response.GetValue("psp_CreatedAt");
