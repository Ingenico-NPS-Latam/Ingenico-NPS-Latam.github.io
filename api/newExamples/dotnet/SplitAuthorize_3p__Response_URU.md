using System;
using NpsSDK;

RootElement response = npsSdk.SplitAuthorize_3p(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_TransactionId");
response.GetValue("psp_Session3p");
response.GetValue("psp_FrontPSP_URL");
response.GetValue("psp_MerchantId");
response.GetValue("psp_MerchTxRef");
response.GetValue("psp_MerchOrderId");
response.GetValue("psp_Amount");
response.GetValue("psp_Currency");
response.GetValue("psp_Country");
response.GetValue("psp_Product");
response.GetValue("psp_PosDateTime");

ComplexElementArray pspTransactions = response.GetComplexElementArray("psp_Transactions");

ComplexElementArrayItem pspTransactions1 = pspTransactions[1];
pspTransactions1.GetValue("psp_MerchantId");
pspTransactions1.GetValue("psp_TransactionId");
pspTransactions1.GetValue("psp_MerchTxRef");
pspTransactions1.GetValue("psp_Product");
pspTransactions1.GetValue("psp_Amount");
pspTransactions1.GetValue("psp_NumPayments");
pspTransactions1.GetValue("psp_CreatedAt");


ComplexElementArrayItem pspTransactions2 = pspTransactions[2];
pspTransactions2.GetValue("psp_MerchantId");
pspTransactions2.GetValue("psp_TransactionId");
pspTransactions2.GetValue("psp_MerchTxRef");
pspTransactions2.GetValue("psp_Product");
pspTransactions2.GetValue("psp_Amount");
pspTransactions2.GetValue("psp_NumPayments");
pspTransactions2.GetValue("psp_CreatedAt");


