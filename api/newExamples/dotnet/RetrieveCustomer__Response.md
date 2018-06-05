using System;
using NpsSDK;

RootElement response = npsSdk.RetrieveCustomer(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_MerchantId");
response.GetValue("psp_CustomerId");
response.GetValue("psp_EmailAddress");
response.GetValue("psp_AlternativeEmailAddress");
response.GetValue("psp_AccountID");
response.GetValue("psp_AccountCreatedAt");
response.GetValue("psp_PosDateTime");
