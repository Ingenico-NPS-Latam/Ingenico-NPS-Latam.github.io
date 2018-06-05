import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.splitPayOnline_3p(data);

response.getValue("psp_ResponseCod");
response.getValue("psp_ResponseMsg");
response.getValue("psp_TransactionId");
response.getValue("psp_Session3p");
response.getValue("psp_FrontPSP_URL");
response.getValue("psp_MerchantId");
response.getValue("psp_MerchTxRef");
response.getValue("psp_MerchOrderId");
response.getValue("psp_Amount");
response.getValue("psp_Currency");
response.getValue("psp_Country");
response.getValue("psp_Product");
response.getValue("psp_PosDateTime");

List<ComplexElementArrayItem> pspTransactions = response.getComplexElementArray('psp_Transactions');

ComplexElementArrayItem pspTransactions1 = pspTransactions.getValue(1);
pspTransactions1.getValue("psp_MerchantId");
pspTransactions1.getValue("psp_TransactionId");
pspTransactions1.getValue("psp_MerchTxRef");
pspTransactions1.getValue("psp_Product");
pspTransactions1.getValue("psp_Amount");
pspTransactions1.getValue("psp_NumPayments");
pspTransactions1.getValue("psp_CreatedAt");


ComplexElementArrayItem pspTransactions2 = pspTransactions.getValue(2);
pspTransactions2.getValue("psp_MerchantId");
pspTransactions2.getValue("psp_TransactionId");
pspTransactions2.getValue("psp_MerchTxRef");
pspTransactions2.getValue("psp_Product");
pspTransactions2.getValue("psp_Amount");
pspTransactions2.getValue("psp_NumPayments");
pspTransactions2.getValue("psp_CreatedAt");


