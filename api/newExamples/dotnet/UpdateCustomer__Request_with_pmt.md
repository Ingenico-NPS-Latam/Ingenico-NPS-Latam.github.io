using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_CustomerId", "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b");
    data.Add("psp_EmailAddress", "jhon.doe@example.com");
    data.Add("psp_AlternativeEmailAddress", "jdoe@example.com");
    data.Add("psp_AccountCreatedAt", "2010-10-23");
    data.Add("psp_AccountID", "jdoe78");

    ComplexElement pspPaymentMethod = new ComplexElement();
    pspPaymentMethod.Add("PaymentMethodToken", "vp1PTJuKCVMXsbeOoAx94gxv2dQM5fUK");

    data.Add("psp_PaymentMethod", pspPaymentMethod);
    data.Add("psp_PosDateTime", "2008-01-12 13:05:00");
    RootElement response = npsSdk.UpdateCustomer(data);

}
catch (Exception ex){
    //Code to handle error
}

