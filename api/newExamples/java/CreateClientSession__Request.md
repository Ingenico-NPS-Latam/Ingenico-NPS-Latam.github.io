import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();

    data.add("psp_Version", "2.2");
    data.add("psp_MerchantId", "sdk_test");
    data.add("psp_PosDateTime", "2019-12-01 12:00:00");
    RootElement response = npsSdk.createClientSession(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
