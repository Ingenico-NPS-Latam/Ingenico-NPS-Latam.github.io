import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();

    data.add("psp_Version", "2.2");
    data.add("psp_MerchantId", "sdk_test");
    data.add("psp_Amount", "100");
    data.add("psp_Product", "14");
    data.add("psp_Currency", "152");
    data.add("psp_Country", "CHL");
    data.add("psp_NumPayments", "1");
    data.add("psp_PaymentMethodToken", "KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM");
    data.add("psp_ClientSession", "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs");
    data.add("psp_PosDateTime", "2017-04-04 13:35:20");
    RootElement response = npsSdk.getInstallmentsOptions(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
