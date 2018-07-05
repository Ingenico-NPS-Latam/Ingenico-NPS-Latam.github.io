{
    ComplexElement pspAmountAdditionalDetails = new ComplexElement();
    pspAmountAdditionalDetails.add("Tip", "20");
    pspAmountAdditionalDetails.add("Discount", "1");

    ComplexElementArray Taxes = new ComplexElementArray();

    ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
    Taxes1.add("TypeId", "600");
    Taxes1.add("Amount", "100");
    Taxes1.add("Rate", "21");
    Taxes1.add("BaseAmount", "10");

    Taxes.add(Taxes1);

    ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
    Taxes2.add("TypeId", "601");
    Taxes2.add("Amount", "100");
    Taxes2.add("Rate", "21");
    Taxes2.add("BaseAmount", "10");

    Taxes.add(Taxes2);

    pspAmountAdditionalDetails.add("Taxes", Taxes);

    data.add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);
}