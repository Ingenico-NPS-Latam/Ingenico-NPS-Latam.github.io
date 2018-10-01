using System;
using NpsSDK;

RootElement response = npsSdk.FraudScreening(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");

ComplexElement pspResult = response.GetComplexElement("psp_Result");
pspResult.GetValue("ResultCode");
pspResult.GetValue("ResultDescription");

response.GetValue("psp_OrderId");
response.GetValue("psp_MerchantId");
response.GetValue("psp_MerchTxRef");
response.GetValue("psp_MerchOrderId");
response.GetValue("psp_Amount");
response.GetValue("psp_NumPayments");
response.GetValue("psp_Currency");
response.GetValue("psp_Country");
response.GetValue("psp_Product");
response.GetValue("psp_CardNumber");
response.GetValue("psp_CardExpDate");
response.GetValue("psp_PosDateTime");
