using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_QueryCriteria", "T");
    data.Add("psp_QueryCriteriaId", "2693310");
    data.Add("psp_PosDateTime", "2019-12-01 12:00:00");
    RootElement response = npsSdk.SimpleQueryTx(data);

}
catch (Exception ex){
    //Code to handle error
}

