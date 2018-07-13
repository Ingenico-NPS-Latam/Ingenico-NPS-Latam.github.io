RootElement data = new RootElement();

data.Add("Tip", "500");
data.Add("Discount", "10000");

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

data.Add("Taxes", Taxes);
