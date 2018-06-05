using System;
using NpsSDK;

RootElement response = npsSdk.CreateClientSession(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_MerchantId");
response.GetValue("psp_ClientSession");
response.GetValue("psp_PosDateTime");
response.GetValue("psp_CreatedAt");
