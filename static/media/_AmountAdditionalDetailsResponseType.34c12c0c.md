ComplexElement pspAmountAdditionalDetails = response.getComplexElement("psp_AmountAdditionalDetails");
pspAmountAdditionalDetails.getValue("Tip");
pspAmountAdditionalDetails.getValue("Discount");

List<ComplexElementArrayItem> taxes = psp_AmountAdditionalDetails.getComplexElementArray('Taxes');

ComplexElementArrayItem taxes1 = taxes.getValue(1);
taxes1.getValue("TypeId");
taxes1.getValue("TypeDescription");
taxes1.getValue("Amount");

ComplexElement rate = taxes1.getComplexElement("Rate");


ComplexElement baseAmount = taxes1.getComplexElement("BaseAmount");


ComplexElement appliedAmount = taxes1.getComplexElement("AppliedAmount");


ComplexElement remarks = taxes1.getComplexElement("Remarks");



ComplexElementArrayItem taxes2 = taxes.getValue(2);
taxes2.getValue("TypeId");
taxes2.getValue("TypeDescription");
taxes2.getValue("Amount");
taxes2.getValue("Rate");
taxes2.getValue("BaseAmount");

ComplexElement appliedAmount = taxes2.getComplexElement("AppliedAmount");


ComplexElement remarks = taxes2.getComplexElement("Remarks");