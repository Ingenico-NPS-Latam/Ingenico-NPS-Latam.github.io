using System;
using NpsSDK;

RootElement response = npsSdk.QueryTxs(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_MerchantId");
response.GetValue("psp_QueryCriteria");
response.GetValue("psp_QueryCriteriaId");
response.GetValue("psp_PosDateTime");

ComplexElementArray pspTransactions = response.GetComplexElementArray("psp_Transactions");

ComplexElementArrayItem pspTransactions1 = pspTransactions[1];
pspTransactions1.GetValue("psp_ResponseCod");
pspTransactions1.GetValue("psp_ResponseMsg");
pspTransactions1.GetValue("psp_ResponseExtended");
pspTransactions1.GetValue("psp_TransactionId");
pspTransactions1.GetValue("psp_MerchantId");
pspTransactions1.GetValue("psp_TxSource");
pspTransactions1.GetValue("psp_Operation");
pspTransactions1.GetValue("psp_MerchTxRef");
pspTransactions1.GetValue("psp_MerchOrderId");
pspTransactions1.GetValue("psp_Amount");
pspTransactions1.GetValue("psp_NumPayments");
pspTransactions1.GetValue("psp_Currency");
pspTransactions1.GetValue("psp_Country");
pspTransactions1.GetValue("psp_Product");
pspTransactions1.GetValue("psp_AuthorizationCode");
pspTransactions1.GetValue("psp_BatchNro");
pspTransactions1.GetValue("psp_TicketNumber");
pspTransactions1.GetValue("psp_CardNumber_FSD");
pspTransactions1.GetValue("psp_CardNumber_LFD");
pspTransactions1.GetValue("psp_CardMask");
pspTransactions1.GetValue("psp_ClExternalMerchant");
pspTransactions1.GetValue("psp_ClExternalTerminal");
pspTransactions1.GetValue("psp_ClResponseCod");
pspTransactions1.GetValue("psp_ClResponseMsg");
pspTransactions1.GetValue("psp_PosDateTime");
pspTransactions1.GetValue("psp_CreatedAt");

ComplexElement pspFraudScreeningResult = pspTransactions1.GetComplexElement("psp_FraudScreeningResult");
pspFraudScreeningResult.GetValue("ResultCode");
pspFraudScreeningResult.GetValue("ResultDescription");


ComplexElement pspVerificationServicesResult = pspTransactions1.GetComplexElement("psp_VerificationServicesResult");
pspVerificationServicesResult.GetValue("ResultCodeCardSecurityCode");
pspVerificationServicesResult.GetValue("ResultCodeBillingAddress");
pspVerificationServicesResult.GetValue("ResultCodeBillingAddressZipCode");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonIDType");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonIDNumber");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonDateOfBirth");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonName");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonPhoneNumber1");
pspVerificationServicesResult.GetValue("ResultCodeCustomerEmailAddress");



ComplexElementArrayItem pspTransactions2 = pspTransactions[2];
pspTransactions2.GetValue("psp_ResponseCod");
pspTransactions2.GetValue("psp_ResponseMsg");
pspTransactions2.GetValue("psp_ResponseExtended");
pspTransactions2.GetValue("psp_TransactionId");
pspTransactions2.GetValue("psp_MerchantId");
pspTransactions2.GetValue("psp_TxSource");
pspTransactions2.GetValue("psp_Operation");
pspTransactions2.GetValue("psp_MerchTxRef");
pspTransactions2.GetValue("psp_MerchOrderId");
pspTransactions2.GetValue("psp_Amount");
pspTransactions2.GetValue("psp_NumPayments");
pspTransactions2.GetValue("psp_Currency");
pspTransactions2.GetValue("psp_Country");
pspTransactions2.GetValue("psp_Product");
pspTransactions2.GetValue("psp_AuthorizationCode");
pspTransactions2.GetValue("psp_BatchNro");
pspTransactions2.GetValue("psp_TicketNumber");
pspTransactions2.GetValue("psp_CardNumber_FSD");
pspTransactions2.GetValue("psp_CardNumber_LFD");
pspTransactions2.GetValue("psp_CardMask");
pspTransactions2.GetValue("psp_ClExternalMerchant");
pspTransactions2.GetValue("psp_ClExternalTerminal");
pspTransactions2.GetValue("psp_ClResponseCod");
pspTransactions2.GetValue("psp_ClResponseMsg");
pspTransactions2.GetValue("psp_PosDateTime");
pspTransactions2.GetValue("psp_CreatedAt");

ComplexElement pspFraudScreeningResult = pspTransactions2.GetComplexElement("psp_FraudScreeningResult");
pspFraudScreeningResult.GetValue("ResultCode");
pspFraudScreeningResult.GetValue("ResultDescription");


ComplexElement pspVerificationServicesResult = pspTransactions2.GetComplexElement("psp_VerificationServicesResult");
pspVerificationServicesResult.GetValue("ResultCodeCardSecurityCode");
pspVerificationServicesResult.GetValue("ResultCodeBillingAddress");
pspVerificationServicesResult.GetValue("ResultCodeBillingAddressZipCode");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonIDType");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonIDNumber");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonDateOfBirth");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonName");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonPhoneNumber1");
pspVerificationServicesResult.GetValue("ResultCodeCustomerEmailAddress");



