using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_TxSource", "WEB");
    data.Add("psp_MerchOrderId", "ORDER66666");
    data.Add("psp_ReturnURL", "http://localhost/");
    data.Add("psp_FrmLanguage", "es_AR");
    data.Add("psp_Amount", "2400000");
    data.Add("psp_Currency", "986");
    data.Add("psp_Country", "BRA");
    data.Add("psp_Product", "14");
    data.Add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElementArray pspTransactions = new ComplexElementArray();

    ComplexElementArrayItem pspTransactions1 = new ComplexElementArrayItem();
    pspTransactions1.Add("psp_MerchantId", "sdk_test");
    pspTransactions1.Add("psp_MerchTxRef", "ORDER66666-3");
    pspTransactions1.Add("psp_Product", "14");
    pspTransactions1.Add("psp_Amount", "1200000");
    pspTransactions1.Add("psp_NumPayments", "1");

    ComplexElement pspAmountAdditionalDetails = new ComplexElement();
    pspAmountAdditionalDetails.Add("Tip", "20");
    pspAmountAdditionalDetails.Add("Discount", "1");

    ComplexElementArray Taxes = new ComplexElementArray();

    ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
    Taxes1.Add("TypeId", "100");
    Taxes1.Add("Amount", "200000");

    Taxes.Add(Taxes1);

    pspAmountAdditionalDetails.Add("Taxes", Taxes);

    pspTransactions1.Add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);

    pspTransactions.Add(pspTransactions1);

    ComplexElementArrayItem pspTransactions2 = new ComplexElementArrayItem();
    pspTransactions2.Add("psp_MerchantId", "sdk_test");
    pspTransactions2.Add("psp_MerchTxRef", "ORDER66666-3");
    pspTransactions2.Add("psp_Product", "14");
    pspTransactions2.Add("psp_Amount", "1200000");
    pspTransactions2.Add("psp_NumPayments", "1");

    ComplexElement pspAmountAdditionalDetails = new ComplexElement();
    pspAmountAdditionalDetails.Add("Tip", "20");
    pspAmountAdditionalDetails.Add("Discount", "1");

    ComplexElementArray Taxes = new ComplexElementArray();

    ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
    Taxes1.Add("TypeId", "100");
    Taxes1.Add("Amount", "200000");

    Taxes.Add(Taxes1);

    pspAmountAdditionalDetails.Add("Taxes", Taxes);

    pspTransactions2.Add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);

    pspTransactions.Add(pspTransactions2);

    data.Add("psp_Transactions", pspTransactions);
    RootElement response = npsSdk.SplitAuthorize_3p(data);

}
catch (Exception ex){
    //Code to handle error
}

