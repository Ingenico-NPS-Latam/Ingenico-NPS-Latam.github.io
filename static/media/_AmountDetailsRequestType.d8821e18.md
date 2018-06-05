using System;
using NpsSDK;

try{

    RootElement data = new RootElement();


    ComplexElement AmountDetailsRequest = new ComplexElement();
    AmountDetailsRequest.Add("Tip", "500");
    AmountDetailsRequest.Add("Discount", "10000");

    ComplexElementArray Taxes = new ComplexElementArray();

    ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
    Taxes1.Add("TypeId", "500");
    Taxes1.Add("Amount", "10000");
    Taxes1.Add("Rate", "2100");
    Taxes1.Add("BaseAmount", "10000");

    Taxes.Add(Taxes1);

    ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
    Taxes2.Add("TypeId", "500");
    Taxes2.Add("Amount", "10000");
    Taxes2.Add("Rate", "2100");
    Taxes2.Add("BaseAmount", "10000");

    Taxes.Add(Taxes2);

    AmountDetailsRequest.Add("Taxes", Taxes);

    data.Add("AmountDetailsRequest", AmountDetailsRequest);
    RootElement response = npsSdk.AmountDetailsRequestType.md(data);

}
catch (Exception ex){
    //Code to handle error
}