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
    data.Add("psp_Amount", "15050");
    data.Add("psp_Currency", "032");
    data.Add("psp_Country", "ARG");
    data.Add("psp_Product", "14");
    data.Add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElement pspVaultReference = new ComplexElement();
    pspVaultReference.Add("CustomerId", "K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f");

    data.Add("psp_VaultReference", pspVaultReference);

    ComplexElementArray pspTransactions = new ComplexElementArray();

    ComplexElementArrayItem pspTransactions1 = new ComplexElementArrayItem();
    pspTransactions1.Add("psp_MerchantId", "sdk_test");
    pspTransactions1.Add("psp_MerchTxRef", "ORDER66666-3");
    pspTransactions1.Add("psp_Product", "14");
    pspTransactions1.Add("psp_Amount", "10000");
    pspTransactions1.Add("psp_NumPayments", "1");

    pspTransactions.Add(pspTransactions1);

    ComplexElementArrayItem pspTransactions2 = new ComplexElementArrayItem();
    pspTransactions2.Add("psp_MerchantId", "sdk_test");
    pspTransactions2.Add("psp_MerchTxRef", "ORDER66666-3");
    pspTransactions2.Add("psp_Product", "14");
    pspTransactions2.Add("psp_Amount", "5050");
    pspTransactions2.Add("psp_NumPayments", "1");

    pspTransactions.Add(pspTransactions2);

    data.Add("psp_Transactions", pspTransactions);
    RootElement response = npsSdk.SplitAuthorize_3p(data);

}
catch (Exception ex){
    //Code to handle error
}

