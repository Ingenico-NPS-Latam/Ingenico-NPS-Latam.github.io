{
ComplexElementArray Taxes = new ComplexElementArray();

ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
Taxes1.add("TypeId", "100");
Taxes1.add("Amount", "100");
Taxes1.add("Rate", "21");
Taxes1.add("BaseAmount", "10");

Taxes.add(Taxes1);

ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
Taxes2.add("TypeId", "500");
Taxes2.add("Amount", "100");
Taxes2.add("Rate", "21");
Taxes2.add("BaseAmount", "10");

Taxes.add(Taxes2);

pspAmountAdditionalDetails.add("Taxes", Taxes);
}