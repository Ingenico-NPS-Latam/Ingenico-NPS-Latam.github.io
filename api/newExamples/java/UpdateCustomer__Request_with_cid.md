import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();

    data.add("psp_Version", "2.2");
    data.add("psp_MerchantId", "sdk_test");
    data.add("psp_CustomerId", "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b");
    data.add("psp_EmailAddress", "jhon.doe@example.com");
    data.add("psp_AlternativeEmailAddress", "jdoe@example.com");
    data.add("psp_AccountCreatedAt", "2010-10-23");
    data.add("psp_AccountID", "jdoe78");

    ComplexElement pspPaymentMethod = new ComplexElement();

    ComplexElement CardInputDetails = new ComplexElement();
    CardInputDetails.add("Number", "4507990000000010");
    CardInputDetails.add("ExpirationDate", "2501");
    CardInputDetails.add("SecurityCode", "123");
    CardInputDetails.add("HolderName", "JOHN DOE");

    pspPaymentMethod.add("CardInputDetails", CardInputDetails);

    data.add("psp_PaymentMethod", pspPaymentMethod);
    data.add("psp_PosDateTime", "2008-01-12 13:05:00");
    RootElement response = npsSdk.updateCustomer(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
