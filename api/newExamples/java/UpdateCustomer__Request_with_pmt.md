import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();

    data.add("psp_Version", "2.2");
    data.add("psp_MerchantId", "sdk_test");
    data.add("psp_CustomerId", "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b");
    data.add("psp_EmailAddress", "jhon.doe@example.com");
    data.add("psp_AlternativeEmailAddress", "jdoe@example.com");
    data.add("psp_AccountCreatedAt", "2010-10-23");
    data.add("psp_AccountID", "jdoe78");

    ComplexElement pspPaymentMethod = new ComplexElement();
    pspPaymentMethod.add("PaymentMethodToken", "vp1PTJuKCVMXsbeOoAx94gxv2dQM5fUK");

    data.add("psp_PaymentMethod", pspPaymentMethod);
    data.add("psp_PosDateTime", "2008-01-12 13:05:00");
    RootElement response = npsSdk.updateCustomer(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
