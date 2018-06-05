using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_Amount", "100");
    data.Add("psp_Product", "14");
    data.Add("psp_Currency", "152");
    data.Add("psp_Country", "CHL");
    data.Add("psp_NumPayments", "1");
    data.Add("psp_PaymentMethodToken", "KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM");
    data.Add("psp_ClientSession", "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs");
    data.Add("psp_PosDateTime", "2017-04-04 13:35:20");
    RootElement response = npsSdk.GetInstallmentsOptions(data);

}
catch (Exception ex){
    //Code to handle error
}

