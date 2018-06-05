using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_PaymentMethodId", "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE");
    data.Add("psp_PaymentMethodTag", "Corporate card");

    ComplexElement pspCardInputDetails = new ComplexElement();
    pspCardInputDetails.Add("ExpirationDate", "2501");

    data.Add("psp_CardInputDetails", pspCardInputDetails);
    data.Add("psp_PosDateTime", "2008-01-12 13:05:00");
    RootElement response = npsSdk.UpdatePaymentMethod(data);

}
catch (Exception ex){
    //Code to handle error
}

