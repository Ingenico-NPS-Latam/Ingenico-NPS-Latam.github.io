using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_TxSource", "WEB");
    data.Add("psp_MerchTxRef", "ORDERX1466Xz-3");
    data.Add("psp_MerchOrderId", "ORDERX1466Xz");
    data.Add("psp_Amount", "1360000");
    data.Add("psp_NumPayments", "1");
    data.Add("psp_Currency", "170");
    data.Add("psp_Country", "COL");
    data.Add("psp_Product", "14");
    data.Add("psp_CardNumber", "4005580000050003");
    data.Add("psp_CardExpDate", "1812");
    data.Add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElement pspAmountAdditionalDetails = new ComplexElement();
    pspAmountAdditionalDetails.Add("Tip", "20");
    pspAmountAdditionalDetails.Add("Discount", "1");

    ComplexElementArray Taxes = new ComplexElementArray();

    ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
    Taxes1.Add("TypeId", "100");
    Taxes1.Add("Amount", "200000");

    Taxes.Add(Taxes1);

    ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
    Taxes2.Add("TypeId", "501");
    Taxes2.Add("Amount", "160000");
    Taxes2.Add("Rate", "1600");
    Taxes2.Add("BaseAmount", "1000000");

    Taxes.Add(Taxes2);

    pspAmountAdditionalDetails.Add("Taxes", Taxes);

    data.Add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);
    RootElement response = npsSdk.PayOnline_2p(data);

}
catch (Exception ex){
    //Code to handle error
}

