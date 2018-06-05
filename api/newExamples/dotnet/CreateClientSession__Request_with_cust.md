using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_PosDateTime", "2019-12-01 12:00:00");
    data.Add("psp_CustomerId", "K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f");
    RootElement response = npsSdk.CreateClientSession(data);

}
catch (Exception ex){
    //Code to handle error
}

