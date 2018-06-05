import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();

    data.add("psp_Version", "2.2");
    data.add("psp_MerchantId", "sdk_test");

    ComplexElement pspCardInputDetails = new ComplexElement();
    pspCardInputDetails.add("Number", "4507990000000010");
    pspCardInputDetails.add("ExpirationDate", "2501");
    pspCardInputDetails.add("SecurityCode", "123");
    pspCardInputDetails.add("HolderName", "JOHN DOE");

    data.add("psp_CardInputDetails", pspCardInputDetails);
    data.add("psp_ClientSession", "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs");
    RootElement response = npsSdk.createPaymentMethodToken(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
