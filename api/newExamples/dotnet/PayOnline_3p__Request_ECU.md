using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "psp_test");
    data.Add("psp_TxSource", "WEB");
    data.Add("psp_MerchTxRef", "ORDER76666-3");
    data.Add("psp_MerchOrderId", "ORDER76666");
    data.Add("psp_ReturnURL", "http://localhost/");
    data.Add("psp_FrmLanguage", "es_AR");
    data.Add("psp_NumPayments", "1");
    data.Add("psp_Currency", "840");
    data.Add("psp_Country", "ECU");
    data.Add("psp_Product", "14");
    data.Add("psp_PosDateTime", "2019-12-01 12:00:00");
    data.Add("psp_Amount", "31200");

    ComplexElement pspAmountAdditionalDetails = new ComplexElement();

    ComplexElementArray Taxes = new ComplexElementArray();

    ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
    Taxes1.Add("TypeId", "700");
    Taxes1.Add("Amount", "1200");
    Taxes1.Add("Rate", "1200");
    Taxes1.Add("BaseAmount", "100000");

    Taxes.Add(Taxes1);

    ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
    Taxes2.Add("TypeId", "701");
    Taxes2.Add("BaseAmount", "20000");

    Taxes.Add(Taxes2);

    pspAmountAdditionalDetails.Add("Taxes", Taxes);

    data.Add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);
    RootElement response = npsSdk.PayOnline_3p(data);

}
catch (Exception ex){
    //Code to handle error
}

