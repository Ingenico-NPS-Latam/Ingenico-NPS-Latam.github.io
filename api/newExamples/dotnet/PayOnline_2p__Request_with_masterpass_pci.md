using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_TxSource", "WEB");
    data.Add("psp_MerchTxRef", "ORDER69461-3");
    data.Add("psp_MerchOrderId", "ORDER69461");
    data.Add("psp_Amount", "15050");
    data.Add("psp_NumPayments", "1");
    data.Add("psp_Currency", "032");
    data.Add("psp_Country", "ARG");
    data.Add("psp_Product", "14");
    data.Add("psp_CardNumber", "4507990000000010");
    data.Add("psp_CardExpDate", "1912");
    data.Add("psp_CardSecurityCode", "325");
    data.Add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElement pspWalletReference = new ComplexElement();
    pspWalletReference.Add("WalletTypeId", "2");
    pspWalletReference.Add("WalletIdentificationCode", "101");

    data.Add("psp_WalletReference", pspWalletReference);
    RootElement response = npsSdk.PayOnline_2p(data);

}
catch (Exception ex){
    //Code to handle error
}

