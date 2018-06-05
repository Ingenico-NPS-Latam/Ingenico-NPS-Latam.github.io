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
    data.add("psp_MerchTxRef", "ORDERX1466Xz-3");
    data.add("psp_MerchOrderId", "ORDERX1466Xz");
    data.add("psp_Amount", "15050");
    data.add("psp_NumPayments", "1");
    data.add("psp_Currency", "032");
    data.add("psp_Country", "ARG");
    data.add("psp_Product", "14");
    data.add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElement pspVaultReference = new ComplexElement();
    pspVaultReference.add("PaymentMethodId", "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE");

    data.add("psp_VaultReference", pspVaultReference);
    RootElement response = npsSdk.authorize_2p(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
