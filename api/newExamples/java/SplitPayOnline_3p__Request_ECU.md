import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();

    data.add("psp_Version", "2.2");
    data.add("psp_MerchantId", "psp_test");
    data.add("psp_TxSource", "WEB");
    data.add("psp_MerchOrderId", "ORDER66666");
    data.add("psp_ReturnURL", "http://localhost/");
    data.add("psp_FrmLanguage", "es_AR");
    data.add("psp_Amount", "62400");
    data.add("psp_Currency", "840");
    data.add("psp_Country", "ECU");
    data.add("psp_Product", "14");
    data.add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElementArray pspTransactions = new ComplexElementArray();

    ComplexElementArrayItem pspTransactions1 = new ComplexElementArrayItem();
    pspTransactions1.add("psp_MerchantId", "psp_test");
    pspTransactions1.add("psp_MerchTxRef", "ORDER66666-3");
    pspTransactions1.add("psp_Product", "14");
    pspTransactions1.add("psp_Amount", "31200");
    pspTransactions1.add("psp_NumPayments", "1");

    ComplexElement pspAmountAdditionalDetails = new ComplexElement();

    ComplexElementArray Taxes = new ComplexElementArray();

    ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
    Taxes1.add("TypeId", "700");
    Taxes1.add("Amount", "1200");
    Taxes1.add("Rate", "1200");
    Taxes1.add("BaseAmount", "10000");

    Taxes.add(Taxes1);

    ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
    Taxes2.add("TypeId", "701");
    Taxes2.add("BaseAmount", "20000");

    Taxes.add(Taxes2);

    pspAmountAdditionalDetails.add("Taxes", Taxes);

    pspTransactions1.add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);

    pspTransactions.add(pspTransactions1);

    ComplexElementArrayItem pspTransactions2 = new ComplexElementArrayItem();
    pspTransactions2.add("psp_MerchantId", "psp_test");
    pspTransactions2.add("psp_MerchTxRef", "ORDER66666-3");
    pspTransactions2.add("psp_Product", "14");
    pspTransactions2.add("psp_Amount", "31200");
    pspTransactions2.add("psp_NumPayments", "1");

    ComplexElement pspAmountAdditionalDetails = new ComplexElement();

    ComplexElementArray Taxes = new ComplexElementArray();

    ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
    Taxes1.add("TypeId", "700");
    Taxes1.add("Amount", "1200");
    Taxes1.add("Rate", "1200");
    Taxes1.add("BaseAmount", "10000");

    Taxes.add(Taxes1);

    ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
    Taxes2.add("TypeId", "701");
    Taxes2.add("BaseAmount", "20000");

    Taxes.add(Taxes2);

    pspAmountAdditionalDetails.add("Taxes", Taxes);

    pspTransactions2.add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);

    pspTransactions.add(pspTransactions2);

    data.add("psp_Transactions", pspTransactions);
    RootElement response = npsSdk.splitPayOnline_3p(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
