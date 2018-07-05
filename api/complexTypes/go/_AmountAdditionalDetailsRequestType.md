{
    pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsStruct()
    pspAmountAdditionalDetails.Tip = "20"
    pspAmountAdditionalDetails.Discount = "1"
    
    ComplexElementArray Taxes = new ComplexElementArray();
    
    ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
    Taxes1.TypeId = "600"
    Taxes1.Amount = "100"
    Taxes1.Rate = "21"
    Taxes1.BaseAmount = "10"
    
    Taxes.add(Taxes1);
    
    ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
    Taxes2.TypeId = "601"
    Taxes2.Amount = "100"
    Taxes2.Rate = "21"
    Taxes2.BaseAmount = "10"
    
    Taxes.add(Taxes2);
    
    pspAmountAdditionalDetails.Taxes = Taxes
}