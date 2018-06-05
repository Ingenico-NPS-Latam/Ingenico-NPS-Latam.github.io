using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_PaymentMethodToken", "KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM");
    data.Add("psp_ClientSession", "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs");
    RootElement response = npsSdk.RetrievePaymentMethodToken(data);

}
catch (Exception ex){
    //Code to handle error
}

