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
response.GetValue("psp_ClTrnId");
response.GetValue("psp_ClExternalMerchant");
response.GetValue("psp_ClExternalTerminal");
response.GetValue("psp_ClResponseCod");
response.GetValue("psp_ClResponseMsg");
response.GetValue("psp_PosDateTime");
response.GetValue("psp_CreatedAt");

ComplexElement pspAmountAdditionalDetails = response.GetComplexElement("psp_AmountAdditionalDetails");

ComplexElementArray taxes = psp_AmountAdditionalDetails.GetComplexElementArray("Taxes");

ComplexElementArrayItem taxes1 = taxes[1];
taxes1.GetValue("TypeId");

ComplexElement typeDescription = taxes1.GetComplexElement("TypeDescription");

taxes1.GetValue("Amount");
taxes1.GetValue("Rate");
taxes1.GetValue("BaseAmount");

ComplexElement appliedAmount = taxes1.GetComplexElement("AppliedAmount");


ComplexElement remarks = taxes1.GetComplexElement("Remarks");



ComplexElementArrayItem taxes2 = taxes[2];
taxes2.GetValue("TypeId");

ComplexElement typeDescription = taxes2.GetComplexElement("TypeDescription");


ComplexElement amount = taxes2.GetComplexElement("Amount");


ComplexElement rate = taxes2.GetComplexElement("Rate");

taxes2.GetValue("BaseAmount");

ComplexElement appliedAmount = taxes2.GetComplexElement("AppliedAmount");


ComplexElement remarks = taxes2.GetComplexElement("Remarks");





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

