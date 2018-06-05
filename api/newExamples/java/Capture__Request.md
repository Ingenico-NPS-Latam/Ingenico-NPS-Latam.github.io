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
    data.add("psp_MerchTxRef", "ORDER66666-3");
    data.add("psp_TransactionId_Orig", "2693348");
    data.add("psp_AmountToCapture", "15050");
    data.add("psp_PosDateTime", "2019-12-01 12:00:00");
    RootElement response = npsSdk.capture(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
