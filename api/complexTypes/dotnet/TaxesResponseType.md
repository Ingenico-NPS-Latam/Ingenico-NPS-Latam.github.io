RootElement data = new RootElement();


ComplexElement Taxes = new ComplexElement();
Taxes.Add("TypeId", "601");
Taxes.Add("TypeDescription", "IVA (Ley 19210)");
Taxes.Add("Amount", "10000");
Taxes.Add("Rate", "1050");
Taxes.Add("BaseAmount", "10000");
Taxes.Add("AppliedAmount", "8500");
Taxes.Add("Remarks", "IVA Ley 19210");

data.Add("Taxes", Taxes);
