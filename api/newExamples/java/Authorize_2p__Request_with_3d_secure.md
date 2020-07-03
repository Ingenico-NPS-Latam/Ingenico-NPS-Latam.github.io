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
    data.add("psp_CardNumber", "4507990000000010");
    data.add("psp_CardExpDate", "1912");
    data.add("psp_PosDateTime", "2019-12-01 12:00:00");
    data.add("psp_3dSecure_XID", "MjY0MjAxNjA4MDIyMDUzMzYyNjU=");
    data.add("psp_3dSecure_CAVV", "AAABBYZ3N5Qhl3kBU3c3ELGUsMY=");
    data.add("psp_3dSecure_ECI", "05");
    data.add("psp_3dSecure_Secured", "1");
    data.Add("psp_3dSecure_ProtocolVersion", "2.1.0");
    data.Add("psp_3dSecure_DirectoryServerTransactionId", "c4e59ceb-a382-4d6a-bc87-385d591fa09d");
    RootElement response = npsSdk.authorize_2p(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
