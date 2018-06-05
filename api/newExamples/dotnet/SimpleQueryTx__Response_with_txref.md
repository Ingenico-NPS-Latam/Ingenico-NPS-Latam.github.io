using System;
using NpsSDK;

RootElement response = npsSdk.SimpleQueryTx(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_MerchantId");
response.GetValue("psp_QueryCriteria");
response.GetValue("psp_QueryCriteriaId");
response.GetValue("psp_PosDateTime");

ComplexElement pspTransaction = response.GetComplexElement("psp_Transaction");
pspTransaction.GetValue("psp_ResponseCod");
pspTransaction.GetValue("psp_ResponseMsg");
pspTransaction.GetValue("psp_ResponseExtended");
pspTransaction.GetValue("psp_TransactionId");
pspTransaction.GetValue("psp_MerchantId");
pspTransaction.GetValue("psp_TxSource");
pspTransaction.GetValue("psp_Operation");
pspTransaction.GetValue("psp_MerchTxRef");
pspTransaction.GetValue("psp_MerchOrderId");
pspTransaction.GetValue("psp_Amount");
pspTransaction.GetValue("psp_NumPayments");
pspTransaction.GetValue("psp_Currency");
pspTransaction.GetValue("psp_Country");
pspTransaction.GetValue("psp_Product");
pspTransaction.GetValue("psp_AuthorizationCode");
pspTransaction.GetValue("psp_BatchNro");
pspTransaction.GetValue("psp_TicketNumber");
pspTransaction.GetValue("psp_CardNumber_FSD");
pspTransaction.GetValue("psp_CardNumber_LFD");
pspTransaction.GetValue("psp_CardMask");
pspTransaction.GetValue("psp_ClExternalMerchant");
pspTransaction.GetValue("psp_ClExternalTerminal");
pspTransaction.GetValue("psp_ClResponseCod");
pspTransaction.GetValue("psp_ClResponseMsg");
pspTransaction.GetValue("psp_PosDateTime");
pspTransaction.GetValue("psp_CreatedAt");

ComplexElement pspFraudScreeningResult = psp_Transaction.GetComplexElement("psp_FraudScreeningResult");
pspFraudScreeningResult.GetValue("ResultCode");
pspFraudScreeningResult.GetValue("ResultDescription");


ComplexElement pspVerificationServicesResult = psp_Transaction.GetComplexElement("psp_VerificationServicesResult");
pspVerificationServicesResult.GetValue("ResultCodeCardSecurityCode");
pspVerificationServicesResult.GetValue("ResultCodeBillingAddress");
pspVerificationServicesResult.GetValue("ResultCodeBillingAddressZipCode");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonIDType");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonIDNumber");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonDateOfBirth");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonName");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonPhoneNumber1");
pspVerificationServicesResult.GetValue("ResultCodeCustomerEmailAddress");


