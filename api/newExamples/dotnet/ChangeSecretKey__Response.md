using System;
using NpsSDK;

RootElement response = npsSdk.ChangeSecretKey(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_MerchantId");
response.GetValue("psp_PosDateTime");
