using System;
using NpsSDK;

RootElement response = npsSdk.QueryCardNumber(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_MerchantId");
response.GetValue("psp_QueryCriteria");
response.GetValue("psp_QueryCriteriaId");
response.GetValue("psp_PosDateTime");
response.GetValue("psp_CardNumber");
