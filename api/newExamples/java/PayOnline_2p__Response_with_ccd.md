import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.payOnline_2p(data);

response.getValue("psp_ResponseCod");
response.getValue("psp_ResponseMsg");
response.getValue("psp_ResponseExtended");
response.getValue("psp_TransactionId");
response.getValue("psp_MerchantId");
response.getValue("psp_MerchTxRef");
response.getValue("psp_MerchOrderId");
response.getValue("psp_Amount");
response.getValue("psp_NumPayments");
response.getValue("psp_Currency");
response.getValue("psp_Country");
response.getValue("psp_Product");
response.getValue("psp_CardNumber");
response.getValue("psp_CardExpDate");
response.getValue("psp_AuthorizationCode");
response.getValue("psp_BatchNro");
response.getValue("psp_TicketNumber");
response.getValue("psp_ClExternalMerchant");
response.getValue("psp_ClExternalTerminal");
response.getValue("psp_ClResponseCod");
response.getValue("psp_ClResponseMsg");
response.getValue("psp_PosDateTime");
response.getValue("psp_CreatedAt");

ComplexElement pspFraudScreeningResult = response.getComplexElement("psp_FraudScreeningResult");
pspFraudScreeningResult.getValue("ResultCode");
pspFraudScreeningResult.getValue("ResultDescription");


ComplexElement pspVerificationServicesResult = response.getComplexElement("psp_VerificationServicesResult");
pspVerificationServicesResult.getValue("ResultCodeCardSecurityCode");
pspVerificationServicesResult.getValue("ResultCodeBillingAddress");
pspVerificationServicesResult.getValue("ResultCodeBillingAddressZipCode");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonIDType");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonIDNumber");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonDateOfBirth");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonName");
pspVerificationServicesResult.getValue("ResultCodeBillingPersonPhoneNumber1");
pspVerificationServicesResult.getValue("ResultCodeCustomerEmailAddress");

