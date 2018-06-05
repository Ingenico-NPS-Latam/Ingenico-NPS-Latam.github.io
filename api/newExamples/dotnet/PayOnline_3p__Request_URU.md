using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_TxSource", "WEB");
    data.Add("psp_MerchTxRef", "ORDER76666-3");
    data.Add("psp_MerchOrderId", "ORDER76666");
    data.Add("psp_ReturnURL", "http://localhost/");
    data.Add("psp_FrmLanguage", "es_AR");
    data.Add("psp_Amount", "1220000");
    data.Add("psp_NumPayments", "1");
    data.Add("psp_Currency", "858");
    data.Add("psp_Country", "URY");
    data.Add("psp_Product", "5");
    data.Add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElement pspAmountAdditionalDetails = new ComplexElement();
    pspAmountAdditionalDetails.Add("Tip", "20");
    pspAmountAdditionalDetails.Add("Discount", "1");

    ComplexElementArray Taxes = new ComplexElementArray();

    ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
    Taxes1.Add("TypeId", "601");
    Taxes1.Add("Amount", "220000");
    Taxes1.Add("Rate", "2200");
    Taxes1.Add("BaseAmount", "1000000");

    Taxes.Add(Taxes1);

    pspAmountAdditionalDetails.Add("Taxes", Taxes);

    data.Add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);

    ComplexElement pspBillingDetails = new ComplexElement();
    pspBillingDetails.Add("Invoice", "A00024144");
    pspBillingDetails.Add("InvoiceAmount", "1600000");
    pspBillingDetails.Add("InvoiceCurrency", "858");

    data.Add("psp_BillingDetails", pspBillingDetails);
    RootElement response = npsSdk.PayOnline_3p(data);

}
catch (Exception ex){
    //Code to handle error
}

