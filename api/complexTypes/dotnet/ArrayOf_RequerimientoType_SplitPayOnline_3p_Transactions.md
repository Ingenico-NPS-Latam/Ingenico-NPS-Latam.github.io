RootElement data = new RootElement();

data.Add("psp_MerchantId", "sdk_test");
data.Add("psp_MerchTxRef", "ORDER1000-1");
data.Add("psp_MerchAdditionalRef", "ADDITIONAL-REF1234");
data.Add("psp_Product", "14");
data.Add("psp_PromotionCode", "VISA SANTANDER");
data.Add("psp_Amount", "15050");
data.Add("psp_NumPayments", "1");
data.Add("psp_SoftDescriptor", "Compra Art 15");

ComplexElement pspAmountAdditionalDetails = new ComplexElement();
pspAmountAdditionalDetails.Add("Tip", "20000");
pspAmountAdditionalDetails.Add("Discount", "11000");

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

pspAmountAdditionalDetails.Add("Taxes", Taxes);

data.Add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);
