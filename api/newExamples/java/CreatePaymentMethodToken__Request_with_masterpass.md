import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();

    data.add("psp_Version", "2.2");
    data.add("psp_MerchantId", "sdk_test");

    ComplexElement pspWalletInputDetails = new ComplexElement();
    pspWalletInputDetails.add("WalletTypeId", "2");
    pspWalletInputDetails.add("WalletKey", "d084703513e87cd1540a114cd7317e6642eca04e");
    pspWalletInputDetails.add("MerchOrderId", "1efed583-1824-436a-869f-286ebdb22ae9");

    data.add("psp_WalletInputDetails", pspWalletInputDetails);
    data.add("psp_ClientSession", "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs");
    RootElement response = npsSdk.createPaymentMethodToken(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
