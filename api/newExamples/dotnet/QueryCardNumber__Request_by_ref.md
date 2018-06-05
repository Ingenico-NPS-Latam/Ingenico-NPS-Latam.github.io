using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "1");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_QueryCriteria", "M");
    data.Add("psp_QueryCriteriaId", "ORDERX1466Xz-3");
    data.Add("psp_PosDateTime", "2019-12-01 12:00:00");
    RootElement response = npsSdk.QueryCardNumber(data);

}
catch (Exception ex){
    //Code to handle error
}

