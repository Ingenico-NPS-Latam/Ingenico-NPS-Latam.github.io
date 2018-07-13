RootElement data = new RootElement();


ComplexElement Taxes = new ComplexElement();
Taxes.add("TypeId", "601");
Taxes.add("TypeDescription", "IVA (Ley 19210)");
Taxes.add("Amount", "10000");
Taxes.add("Rate", "1050");
Taxes.add("BaseAmount", "10000");
Taxes.add("AppliedAmount", "8500");
Taxes.add("Remarks", "IVA Ley 19210");

data.add("Taxes", Taxes);
