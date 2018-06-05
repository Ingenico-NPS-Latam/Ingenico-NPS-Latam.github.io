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
    data.add("psp_MerchTxRef", "ORDERX1466Xz-3");
    data.add("psp_MerchOrderId", "ORDERX1466Xz");
    data.add("psp_Amount", "1360000");
    data.add("psp_NumPayments", "1");
    data.add("psp_Currency", "170");
    data.add("psp_Country", "COL");
    data.add("psp_Product", "14");
    data.add("psp_CardNumber", "4005580000050003");
    data.add("psp_CardExpDate", "1812");
    data.add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElement pspAmountAdditionalDetails = new ComplexElement();
    pspAmountAdditionalDetails.add("Tip", "20");
    pspAmountAdditionalDetails.add("Discount", "1");

    ComplexElementArray Taxes = new ComplexElementArray();

    ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
    Taxes1.add("TypeId", "100");
    Taxes1.add("Amount", "200000");

    Taxes.add(Taxes1);

    ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
    Taxes2.add("TypeId", "501");
    Taxes2.add("Amount", "160000");
    Taxes2.add("Rate", "1600");
    Taxes2.add("BaseAmount", "1000000");

    Taxes.add(Taxes2);

    pspAmountAdditionalDetails.add("Taxes", Taxes);

    data.add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);
    RootElement response = npsSdk.payOnline_2p(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
