using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_TxSource", "WEB");
    data.Add("psp_MerchTxRef", "ORDERX1466Xz-3");
    data.Add("psp_MerchOrderId", "ORDERX1466Xz");
    data.Add("psp_Amount", "15050");
    data.Add("psp_NumPayments", "1");
    data.Add("psp_Currency", "032");
    data.Add("psp_Country", "ARG");
    data.Add("psp_Product", "5");
    data.Add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElement pspVaultReference = new ComplexElement();
    pspVaultReference.Add("PaymentMethodToken", "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE");

    data.Add("psp_VaultReference", pspVaultReference);
    RootElement response = npsSdk.Authorize_2p(data);

}
catch (Exception ex){
    //Code to handle error
}

