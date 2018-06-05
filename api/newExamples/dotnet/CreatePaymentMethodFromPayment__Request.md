using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_TransactionId", "65340022");
    data.Add("psp_PaymentMethodTag", "Corporate card");
    data.Add("psp_PosDateTime", "2008-01-12 13:05:00");
    RootElement response = npsSdk.CreatePaymentMethodFromPayment(data);

}
catch (Exception ex){
    //Code to handle error
}

