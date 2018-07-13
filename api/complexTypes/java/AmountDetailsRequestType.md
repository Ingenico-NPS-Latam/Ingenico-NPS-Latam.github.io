RootElement data = new RootElement();

data.add("Tip", "500");
data.add("Discount", "10000");

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

data.add("Taxes", Taxes);
