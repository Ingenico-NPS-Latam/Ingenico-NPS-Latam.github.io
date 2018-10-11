using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");

    ComplexElement pspWalletInputDetails = new ComplexElement();
    pspWalletInputDetails.Add("WalletTypeId", "2");
    pspWalletInputDetails.Add("WalletKey", "d084703513e87cd1540a114cd7317e6642eca04e");
    pspWalletInputDetails.Add("MerchOrderId", "1efed583-1824-436a-869f-286ebdb22ae9");

    data.Add("psp_WalletInputDetails", pspWalletInputDetails);
    data.Add("psp_ClientSession", "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs");
    RootElement response = npsSdk.CreatePaymentMethodToken(data);

}
catch (Exception ex){
    //Code to handle error
}

