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
    data.add("psp_MerchTxRef", "ORDER32145-3");
    data.add("psp_MerchOrderId", "ORDER32145");
    data.add("psp_ReturnURL", "http://localhost/");
    data.add("psp_FrmLanguage", "es_AR");
    data.add("psp_Amount", "15050");
    data.add("psp_Currency", "032");
    data.add("psp_Country", "ARG");
    data.add("psp_Product", "301");
    data.add("psp_PosDateTime", "2019-12-01 12:00:00");
    data.add("psp_FirstExpDate", "2020-01-01");
    RootElement response = npsSdk.cashPayment_3p(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
