import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();

    data.add("psp_Version", "2.2");
    data.add("psp_MerchantId", "sdk_test");
    data.add("psp_TxSource", "WEB");
    data.add("psp_MerchOrderId", "ORDER66666");
    data.add("psp_ReturnURL", "http://localhost/");
    data.add("psp_FrmLanguage", "es_AR");
    data.add("psp_Amount", "15050");
    data.add("psp_Currency", "032");
    data.add("psp_Country", "ARG");
    data.add("psp_Product", "14");
    data.add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElementArray pspTransactions = new ComplexElementArray();

    ComplexElementArrayItem pspTransactions1 = new ComplexElementArrayItem();
    pspTransactions1.add("psp_MerchantId", "sdk_test");
    pspTransactions1.add("psp_MerchTxRef", "ORDER66666-3");
    pspTransactions1.add("psp_Product", "14");
    pspTransactions1.add("psp_Amount", "10000");
    pspTransactions1.add("psp_NumPayments", "1");

    pspTransactions.add(pspTransactions1);

    ComplexElementArrayItem pspTransactions2 = new ComplexElementArrayItem();
    pspTransactions2.add("psp_MerchantId", "psp_test");
    pspTransactions2.add("psp_MerchTxRef", "ORDER66666-3");
    pspTransactions2.add("psp_Product", "14");
    pspTransactions2.add("psp_Amount", "5050");
    pspTransactions2.add("psp_NumPayments", "12");

    pspTransactions.add(pspTransactions2);

    data.add("psp_Transactions", pspTransactions);
    RootElement response = npsSdk.splitAuthorize_3p(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
