using System;
using NpsSDK;

RootElement response = npsSdk.NotifyFraudScreeningReview(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_ResponseExtended");
response.GetValue("psp_MerchantId");
response.GetValue("psp_PosDateTime");
