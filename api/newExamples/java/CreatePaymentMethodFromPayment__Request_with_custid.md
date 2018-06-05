import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();

    data.add("psp_Version", "2.2");
    data.add("psp_MerchantId", "sdk_test");
    data.add("psp_TransactionId", "65340022");
    data.add("psp_PaymentMethodTag", "Corporate card");
    data.add("psp_CustomerId", "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b");
    data.add("psp_SetAsCustomerDefault", "1");
    data.add("psp_PosDateTime", "2008-01-12 13:05:00");
    RootElement response = npsSdk.createPaymentMethodFromPayment(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
