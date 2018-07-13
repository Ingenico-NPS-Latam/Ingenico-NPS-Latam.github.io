RootElement data = new RootElement();


ComplexElement Taxes = new ComplexElement();
Taxes.Add("TypeId", "500");
Taxes.Add("Amount", "10000");
Taxes.Add("Rate", "2100");
Taxes.Add("BaseAmount", "10000");

data.Add("Taxes", Taxes);
