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
    data.add("psp_MerchTxRef", "ORDER69461-3");
    data.add("psp_MerchOrderId", "ORDER69461");
    data.add("psp_Amount", "1200000");
    data.add("psp_NumPayments", "1");
    data.add("psp_Currency", "986");
    data.add("psp_Country", "BRA");
    data.add("psp_Product", "14");
    data.add("psp_CardNumber", "4507990000000010");
    data.add("psp_CardExpDate", "1912");
    data.add("psp_CardSecurityCode", "325");
    data.add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElement pspAmountAdditionalDetails = new ComplexElement();
    pspAmountAdditionalDetails.add("Tip", "20");
    pspAmountAdditionalDetails.add("Discount", "1");

    ComplexElementArray Taxes = new ComplexElementArray();

    ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
    Taxes1.add("TypeId", "100");
    Taxes1.add("Amount", "200000");

    Taxes.add(Taxes1);

    pspAmountAdditionalDetails.add("Taxes", Taxes);

    data.add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);
    RootElement response = npsSdk.payOnline_2p(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
