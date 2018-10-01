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
    data.add("psp_MerchTxRef", "ORDER66666-3");
    data.add("psp_MerchOrderId", "ORDER66666");
    data.add("psp_Amount", "15050");
    data.add("psp_NumPayments", "1");
    data.add("psp_Currency", "032");
    data.add("psp_Country", "ARG");
    data.add("psp_Product", "14");
    data.add("psp_CardNumber", "4507990000000010");
    data.add("psp_CardExpDate", "1912");
    data.add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElement pspCustomerAdditionalDetails = new ComplexElement();
    pspCustomerAdditionalDetails.add("DeviceFingerPrint", "KJhKHKJgh7777kgh...");

    data.add("psp_CustomerAdditionalDetails", pspCustomerAdditionalDetails);
    RootElement response = npsSdk.fraudScreening(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
