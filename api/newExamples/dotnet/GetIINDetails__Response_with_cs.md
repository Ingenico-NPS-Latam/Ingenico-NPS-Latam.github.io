using System;
using NpsSDK;

RootElement response = npsSdk.GetIINDetails(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_MerchantId");
response.GetValue("psp_Product");
response.GetValue("psp_PosDateTime");
