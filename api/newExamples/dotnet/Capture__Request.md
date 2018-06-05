using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_TxSource", "WEB");
    data.Add("psp_MerchTxRef", "ORDER66666-3");
    data.Add("psp_TransactionId_Orig", "2693348");
    data.Add("psp_AmountToCapture", "15050");
    data.Add("psp_PosDateTime", "2019-12-01 12:00:00");
    RootElement response = npsSdk.Capture(data);

}
catch (Exception ex){
    //Code to handle error
}

