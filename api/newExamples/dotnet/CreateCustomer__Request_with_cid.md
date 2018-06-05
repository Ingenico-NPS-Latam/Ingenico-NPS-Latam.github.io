using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_EmailAddress", "jhon.doe@example.com");
    data.Add("psp_AlternativeEmailAddress", "jdoe@example.com");
    data.Add("psp_AccountID", "jdoe78");
    data.Add("psp_AccountCreatedAt", "2010-10-23");

    ComplexElement pspPaymentMethod = new ComplexElement();

    ComplexElement CardInputDetails = new ComplexElement();
    CardInputDetails.Add("Number", "4507990000000010");
    CardInputDetails.Add("ExpirationDate", "2501");
    CardInputDetails.Add("SecurityCode", "123");
    CardInputDetails.Add("HolderName", "JOHN DOE");

    pspPaymentMethod.Add("CardInputDetails", CardInputDetails);

    data.Add("psp_PaymentMethod", pspPaymentMethod);
    data.Add("psp_PosDateTime", "2008-01-12 13:05:00");
    RootElement response = npsSdk.CreateCustomer(data);

}
catch (Exception ex){
    //Code to handle error
}

