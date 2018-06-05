using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");

    ComplexElement pspCardInputDetails = new ComplexElement();
    pspCardInputDetails.Add("Number", "4507990000000010");
    pspCardInputDetails.Add("ExpirationDate", "2501");
    pspCardInputDetails.Add("SecurityCode", "123");
    pspCardInputDetails.Add("HolderName", "JOHN DOE");

    data.Add("psp_CardInputDetails", pspCardInputDetails);
    data.Add("psp_ClientSession", "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs");
    RootElement response = npsSdk.CreatePaymentMethodToken(data);

}
catch (Exception ex){
    //Code to handle error
}

