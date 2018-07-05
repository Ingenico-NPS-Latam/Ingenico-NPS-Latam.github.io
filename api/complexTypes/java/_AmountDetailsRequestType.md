import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();


    ComplexElement AmountDetailsRequest = new ComplexElement();
    AmountDetailsRequest.add("Tip", "500");
    AmountDetailsRequest.add("Discount", "10000");

    ComplexElementArray Taxes = new ComplexElementArray();

    ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
    Taxes1.add("TypeId", "500");
    Taxes1.add("Amount", "10000");
    Taxes1.add("Rate", "2100");
    Taxes1.add("BaseAmount", "10000");

    Taxes.add(Taxes1);

    ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
    Taxes2.add("TypeId", "500");
    Taxes2.add("Amount", "10000");
    Taxes2.add("Rate", "2100");
    Taxes2.add("BaseAmount", "10000");

    Taxes.add(Taxes2);

    AmountDetailsRequest.add("Taxes", Taxes);

    data.add("AmountDetailsRequest", AmountDetailsRequest);
    RootElement response = npsSdk.amountDetailsRequestType.md(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}