import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.queryTxs(data);

response.getValue("psp_ResponseCod");
response.getValue("psp_ResponseMsg");
response.getValue("psp_MerchantId");
response.getValue("psp_QueryCriteria");
response.getValue("psp_QueryCriteriaId");
response.getValue("psp_PosDateTime");

List<ComplexElementArrayItem> pspTransactions = response.getComplexElementArray('psp_Transactions');

ComplexElementArrayItem pspTransactions1 = pspTransactions.getValue(1);
pspTransactions1.getValue("psp_ResponseCod");
pspTransactions1.getValue("psp_ResponseMsg");
pspTransactions1.getValue("psp_ResponseExtended");
pspTransactions1.getValue("psp_TransactionId");
pspTransactions1.getValue("psp_MerchantId");
pspTransactions1.getValue("psp_TxSource");
pspTransactions1.getValue("psp_Operation");
pspTransactions1.getValue("psp_MerchTxRef");
pspTransactions1.getValue("psp_MerchOrderId");
pspTransactions1.getValue("psp_Amount");
pspTransactions1.getValue("psp_NumPayments");
pspTransactions1.getValue("psp_Currency");
pspTransactions1.getValue("psp_Country");
pspTransactions1.getValue("psp_Product");
pspTransactions1.getValue("psp_AuthorizationCode");
pspTransactions1.getValue("psp_BatchNro");
pspTransactions1.getValue("psp_TicketNumber");
pspTransactions1.getValue("psp_CardNumber_FSD");
pspTransactions1.getValue("psp_CardNumber_LFD");
pspTransactions1.getValue("psp_CardMask");
pspTransactions1.getValue("psp_ClExternalMerchant");
pspTransactions1.getValue("psp_ClExternalTerminal");
pspTransactions1.getValue("psp_ClResponseCod");
pspTransactions1.getValue("psp_ClResponseMsg");
pspTransactions1.getValue("psp_PosDateTime");
pspTransactions1.getValue("psp_CreatedAt");

ComplexElement pspFraudScreeningResult = pspTransactions1.getComplexElement("psp_FraudScreeningResult");
pspFraudScreeningResult.getValue("ResultCode");
pspFraudScreeningResult.getValue("ResultDescription");


ComplexElement pspVerificationServicesResult = pspTransactions1.getComplexElement("psp_VerificationServicesResult");
pspVerificationServicesResult.getValue("ResultCodeCardSecurityCode");
pspVerificationServicesResult.getValue("ResultCodeBillingAddress");
pspVerificationServicesResult.getValue("ResultCodeBillingAddressZipCode");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonIDType");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonIDNumber");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonDateOfBirth");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonName");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonPhoneNumber1");
pspVerificationServicesResult.getValue("ResultCodeCustomerEmailAddress");



ComplexElementArrayItem pspTransactions2 = pspTransactions.getValue(2);
pspTransactions2.getValue("psp_ResponseCod");
pspTransactions2.getValue("psp_ResponseMsg");
pspTransactions2.getValue("psp_ResponseExtended");
pspTransactions2.getValue("psp_TransactionId");
pspTransactions2.getValue("psp_MerchantId");
pspTransactions2.getValue("psp_TxSource");
pspTransactions2.getValue("psp_Operation");
pspTransactions2.getValue("psp_MerchTxRef");
pspTransactions2.getValue("psp_MerchOrderId");
pspTransactions2.getValue("psp_Amount");
pspTransactions2.getValue("psp_NumPayments");
pspTransactions2.getValue("psp_Currency");
pspTransactions2.getValue("psp_Country");
pspTransactions2.getValue("psp_Product");
pspTransactions2.getValue("psp_AuthorizationCode");
pspTransactions2.getValue("psp_BatchNro");
pspTransactions2.getValue("psp_TicketNumber");
pspTransactions2.getValue("psp_CardNumber_FSD");
pspTransactions2.getValue("psp_CardNumber_LFD");
pspTransactions2.getValue("psp_CardMask");
pspTransactions2.getValue("psp_ClExternalMerchant");
pspTransactions2.getValue("psp_ClExternalTerminal");
pspTransactions2.getValue("psp_ClResponseCod");
pspTransactions2.getValue("psp_ClResponseMsg");
pspTransactions2.getValue("psp_PosDateTime");
pspTransactions2.getValue("psp_CreatedAt");

ComplexElement pspFraudScreeningResult = pspTransactions2.getComplexElement("psp_FraudScreeningResult");
pspFraudScreeningResult.getValue("ResultCode");
pspFraudScreeningResult.getValue("ResultDescription");


ComplexElement pspVerificationServicesResult = pspTransactions2.getComplexElement("psp_VerificationServicesResult");
pspVerificationServicesResult.getValue("ResultCodeCardSecurityCode");
pspVerificationServicesResult.getValue("ResultCodeBillingAddress");
pspVerificationServicesResult.getValue("ResultCodeBillingAddressZipCode");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonIDType");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonIDNumber");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonDateOfBirth");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonName");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonPhoneNumber1");
pspVerificationServicesResult.getValue("ResultCodeCustomerEmailAddress");



