using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_PaymentMethodId", "jGW24iDaoMBzfKHViL18TmHo9sHBgW4J");
    data.Add("psp_PosDateTime", "2008-01-12 13:05:00");
    RootElement response = npsSdk.RetrievePaymentMethod(data);

}
catch (Exception ex){
    //Code to handle error
}

