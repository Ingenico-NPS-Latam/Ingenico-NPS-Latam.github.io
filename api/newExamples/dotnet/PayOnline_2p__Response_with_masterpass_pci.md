using System;
using NpsSDK;

RootElement response = npsSdk.PayOnline_2p(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_ResponseExtended");
response.GetValue("psp_TransactionId");
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
response.GetValue("psp_AuthorizationCode");
response.GetValue("psp_BatchNro");
response.GetValue("psp_TicketNumber");
response.GetValue("psp_ClExternalMerchant");
response.GetValue("psp_ClExternalTerminal");
response.GetValue("psp_ClResponseCod");
response.GetValue("psp_ClResponseMsg");
response.GetValue("psp_PosDateTime");
response.GetValue("psp_CreatedAt");

ComplexElement pspFraudScreeningResult = response.GetComplexElement("psp_FraudScreeningResult");
pspFraudScreeningResult.GetValue("ResultCode");
pspFraudScreeningResult.GetValue("ResultDescription");


ComplexElement pspVerificationServicesResult = response.GetComplexElement("psp_VerificationServicesResult");
pspVerificationServicesResult.GetValue("ResultCodeCardSecurityCode");
pspVerificationServicesResult.GetValue("ResultCodeBillingAddress");
pspVerificationServicesResult.GetValue("ResultCodeBillingAddressZipCode");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonIDType");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonIDNumber");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonDateOfBirth");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonName");
pspVerificationServicesResult.GetValue("ResultCodeBillingPersonPhoneNumber1");
pspVerificationServicesResult.GetValue("ResultCodeCustomerEmailAddress");

