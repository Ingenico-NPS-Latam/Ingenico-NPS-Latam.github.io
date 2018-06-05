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
    data.add("psp_PaymentMethodTag", "Corporate card");

    ComplexElement pspCardInputDetails = new ComplexElement();
    pspCardInputDetails.add("ExpirationDate", "2501");

    data.add("psp_CardInputDetails", pspCardInputDetails);
    data.add("psp_PosDateTime", "2008-01-12 13:05:00");
    RootElement response = npsSdk.updatePaymentMethod(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
