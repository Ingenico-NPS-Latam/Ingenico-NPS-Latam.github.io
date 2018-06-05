using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_TxSource", "WEB");
    data.Add("psp_MerchTxRef", "ORDER32145-3");
    data.Add("psp_MerchOrderId", "ORDER32145");
    data.Add("psp_ReturnURL", "http://localhost/");
    data.Add("psp_FrmLanguage", "es_AR");
    data.Add("psp_Amount", "15050");
    data.Add("psp_Currency", "032");
    data.Add("psp_Country", "ARG");
    data.Add("psp_Product", "301");
    data.Add("psp_PosDateTime", "2019-12-01 12:00:00");
    data.Add("psp_FirstExpDate", "2020-01-01");
    RootElement response = npsSdk.CashPayment_3p(data);

}
catch (Exception ex){
    //Code to handle error
}

