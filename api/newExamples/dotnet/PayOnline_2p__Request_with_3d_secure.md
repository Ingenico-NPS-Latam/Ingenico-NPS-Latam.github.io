using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_TxSource", "WEB");
    data.Add("psp_MerchTxRef", "ORDER69461-3");
    data.Add("psp_MerchOrderId", "ORDER69461");
    data.Add("psp_Amount", "15050");
    data.Add("psp_NumPayments", "1");
    data.Add("psp_Currency", "032");
    data.Add("psp_Country", "ARG");
    data.Add("psp_Product", "14");
    data.Add("psp_CardNumber", "4507990000000010");
    data.Add("psp_CardExpDate", "1912");
    data.Add("psp_CardSecurityCode", "325");
    data.Add("psp_PosDateTime", "2019-12-01 12:00:00");
    data.Add("psp_3dSecure_XID", "MjY0MjAxNjA4MDIyMDUzMzYyNjU=");
    data.Add("psp_3dSecure_CAVV", "AAABBYZ3N5Qhl3kBU3c3ELGUsMY=");
    data.Add("psp_3dSecure_ECI", "05");
    data.Add("psp_3dSecure_Secured", "1");
    data.Add("psp_3dSecure_ProtocolVersion", "2.1.0");
    data.Add("psp_3dSecure_DirectoryServerTransactionId", "c4e59ceb-a382-4d6a-bc87-385d591fa09d");
    RootElement response = npsSdk.PayOnline_2p(data);

}
catch (Exception ex){
    //Code to handle error
}

