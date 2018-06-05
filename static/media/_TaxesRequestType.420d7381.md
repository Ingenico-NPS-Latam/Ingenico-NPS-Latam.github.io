{
ComplexElementArray Taxes = new ComplexElementArray();

ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
Taxes1.Add("TypeId", "100");
Taxes1.Add("Amount", "100");
Taxes1.Add("Rate", "21");
Taxes1.Add("BaseAmount", "10");

Taxes.Add(Taxes1);

ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
Taxes2.Add("TypeId", "500");
Taxes2.Add("Amount", "100");
Taxes2.Add("Rate", "21");
Taxes2.Add("BaseAmount", "10");

Taxes.Add(Taxes2);

pspAmountAdditionalDetails.Add("Taxes", Taxes);
}