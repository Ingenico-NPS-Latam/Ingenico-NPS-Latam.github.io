import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.simpleQueryTx(data);

response.getValue("psp_ResponseCod");
response.getValue("psp_ResponseMsg");
response.getValue("psp_MerchantId");
response.getValue("psp_QueryCriteria");
response.getValue("psp_QueryCriteriaId");
response.getValue("psp_PosDateTime");

ComplexElement pspTransaction = response.getComplexElement("psp_Transaction");
pspTransaction.getValue("psp_ResponseCod");
pspTransaction.getValue("psp_ResponseMsg");
pspTransaction.getValue("psp_ResponseExtended");
pspTransaction.getValue("psp_TransactionId");
pspTransaction.getValue("psp_MerchantId");
pspTransaction.getValue("psp_TxSource");
pspTransaction.getValue("psp_Operation");
pspTransaction.getValue("psp_MerchTxRef");
pspTransaction.getValue("psp_MerchOrderId");
pspTransaction.getValue("psp_Amount");
pspTransaction.getValue("psp_NumPayments");
pspTransaction.getValue("psp_Currency");
pspTransaction.getValue("psp_Country");
pspTransaction.getValue("psp_Product");
pspTransaction.getValue("psp_AuthorizationCode");
pspTransaction.getValue("psp_BatchNro");
pspTransaction.getValue("psp_TicketNumber");
pspTransaction.getValue("psp_CardNumber_FSD");
pspTransaction.getValue("psp_CardNumber_LFD");
pspTransaction.getValue("psp_CardMask");
pspTransaction.getValue("psp_ClExternalMerchant");
pspTransaction.getValue("psp_ClExternalTerminal");
pspTransaction.getValue("psp_ClResponseCod");
pspTransaction.getValue("psp_ClResponseMsg");
pspTransaction.getValue("psp_PosDateTime");
pspTransaction.getValue("psp_CreatedAt");

ComplexElement pspFraudScreeningResult = psp_Transaction.getComplexElement("psp_FraudScreeningResult");
pspFraudScreeningResult.getValue("ResultCode");
pspFraudScreeningResult.getValue("ResultDescription");


ComplexElement pspVerificationServicesResult = psp_Transaction.getComplexElement("psp_VerificationServicesResult");
pspVerificationServicesResult.getValue("ResultCodeCardSecurityCode");
pspVerificationServicesResult.getValue("ResultCodeBillingAddress");
pspVerificationServicesResult.getValue("ResultCodeBillingAddressZipCode");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonIDType");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonIDNumber");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonDateOfBirth");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonName");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonPhoneNumber1");
pspVerificationServicesResult.getValue("ResultCodeCustomerEmailAddress");


