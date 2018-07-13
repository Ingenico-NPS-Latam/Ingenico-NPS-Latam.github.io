RootElement data = new RootElement();

data.add("psp_MerchantId", "sdk_test");
data.add("psp_MerchTxRef", "ORDER1000-1");
data.add("psp_MerchAdditionalRef", "ADDITIONAL-REF1234");
data.add("psp_Product", "14");
data.add("psp_PromotionCode", "VISA SANTANDER");
data.add("psp_Amount", "15050");
data.add("psp_NumPayments", "1");
data.add("psp_SoftDescriptor", "Compra Art 15");

ComplexElement pspAmountAdditionalDetails = new ComplexElement();
pspAmountAdditionalDetails.add("Tip", "20000");
pspAmountAdditionalDetails.add("Discount", "11000");

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

pspAmountAdditionalDetails.add("Taxes", Taxes);

data.add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);
