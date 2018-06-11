using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_Criteria", "T");
    data.Add("psp_CriteriaId", "ORDER69461-3");
    data.Add("psp_ReviewResult", "D");
    data.Add("psp_PosDateTime", "2019-12-01 12:00:00");
    RootElement response = npsSdk.NotifyFraudScreeningReview(data);

}
catch (Exception ex){
    //Code to handle error
}

