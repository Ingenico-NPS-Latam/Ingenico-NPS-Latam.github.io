RootElement data = new RootElement();


ComplexElement Taxes = new ComplexElement();
Taxes.add("TypeId", "500");
Taxes.add("Amount", "10000");
Taxes.add("Rate", "2100");
Taxes.add("BaseAmount", "10000");

data.add("Taxes", Taxes);
