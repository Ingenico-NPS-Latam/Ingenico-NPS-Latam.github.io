import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();

    data.add("psp_Version", "2.2");
    data.add("psp_MerchantId", "sdk_test");
    data.add("psp_TxSource", "WEB");
    data.add("psp_MerchOrderId", "ORDER66666");
    data.add("psp_ReturnURL", "http://localhost/");
    data.add("psp_FrmLanguage", "es_AR");
    data.add("psp_Amount", "2440000");
    data.add("psp_Currency", "858");
    data.add("psp_Country", "URY");
    data.add("psp_Product", "5");
    data.add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElement pspBillingDetails = new ComplexElement();
    pspBillingDetails.add("Invoice", "A00024144");
    pspBillingDetails.add("InvoiceAmount", "1600000");
    pspBillingDetails.add("InvoiceCurrency", "858");

    data.add("psp_BillingDetails", pspBillingDetails);

    ComplexElementArray pspTransactions = new ComplexElementArray();

    ComplexElementArrayItem pspTransactions1 = new ComplexElementArrayItem();
    pspTransactions1.add("psp_MerchantId", "sdk_test");
    pspTransactions1.add("psp_MerchTxRef", "ORDER66666-3");
    pspTransactions1.add("psp_Product", "5");
    pspTransactions1.add("psp_Amount", "1220000");
    pspTransactions1.add("psp_NumPayments", "1");

    ComplexElement pspAmountAdditionalDetails = new ComplexElement();
    pspAmountAdditionalDetails.add("Tip", "20");
    pspAmountAdditionalDetails.add("Discount", "1");

    ComplexElementArray Taxes = new ComplexElementArray();

    ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
    Taxes1.add("TypeId", "601");
    Taxes1.add("Amount", "220000");
    Taxes1.add("Rate", "2200");
    Taxes1.add("BaseAmount", "1000000");

    Taxes.add(Taxes1);

    pspAmountAdditionalDetails.add("Taxes", Taxes);

    pspTransactions1.add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);

    pspTransactions.add(pspTransactions1);

    ComplexElementArrayItem pspTransactions2 = new ComplexElementArrayItem();
    pspTransactions2.add("psp_MerchantId", "sdk_test");
    pspTransactions2.add("psp_MerchTxRef", "ORDER66666-3");
    pspTransactions2.add("psp_Product", "5");
    pspTransactions2.add("psp_Amount", "1220000");
    pspTransactions2.add("psp_NumPayments", "1");

    ComplexElement pspAmountAdditionalDetails = new ComplexElement();
    pspAmountAdditionalDetails.add("Tip", "20");
    pspAmountAdditionalDetails.add("Discount", "1");

    ComplexElementArray Taxes = new ComplexElementArray();

    ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
    Taxes1.add("TypeId", "601");
    Taxes1.add("Amount", "220000");
    Taxes1.add("Rate", "2200");
    Taxes1.add("BaseAmount", "1000000");

    Taxes.add(Taxes1);

    pspAmountAdditionalDetails.add("Taxes", Taxes);

    pspTransactions2.add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);

    pspTransactions.add(pspTransactions2);

    data.add("psp_Transactions", pspTransactions);
    RootElement response = npsSdk.splitAuthorize_3p(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
