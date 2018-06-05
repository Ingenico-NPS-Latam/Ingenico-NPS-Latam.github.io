import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();

    data.add("psp_Version", "2.2");
    data.add("psp_MerchantId", "sdk_test");
    data.add("psp_PaymentMethodId", "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE");
    data.add("psp_CardSecurityCode", "123");
    data.add("psp_ClientSession", "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs");
    RootElement response = npsSdk.recachePaymentMethodToken(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
