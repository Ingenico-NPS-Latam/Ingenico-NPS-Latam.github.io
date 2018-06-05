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
    data.add("psp_MerchTxRef", "ORDER76666-3");
    data.add("psp_MerchOrderId", "ORDER76666");
    data.add("psp_NumPayments", "1");
    data.add("psp_ReturnURL", "http://localhost/");
    data.add("psp_FrmLanguage", "es_AR");
    data.add("psp_Amount", "15050");
    data.add("psp_Currency", "032");
    data.add("psp_Country", "ARG");
    data.add("psp_Product", "14");

    ComplexElement pspVaultReference = new ComplexElement();
    pspVaultReference.add("CustomerId", "K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f");

    data.add("psp_VaultReference", pspVaultReference);
    data.add("psp_PosDateTime", "2019-12-01 12:00:00");
    RootElement response = npsSdk.authorize_3p(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
