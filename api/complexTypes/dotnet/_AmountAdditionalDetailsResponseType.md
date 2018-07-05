ComplexElement pspAmountAdditionalDetails = response.GetComplexElement("psp_AmountAdditionalDetails");
pspAmountAdditionalDetails.GetValue("Tip");
pspAmountAdditionalDetails.GetValue("Discount");

ComplexElementArray taxes = psp_AmountAdditionalDetails.GetComplexElementArray("Taxes");

ComplexElementArrayItem taxes1 = taxes[1];
taxes1.GetValue("TypeId");
taxes1.GetValue("TypeDescription");
taxes1.GetValue("Amount");

ComplexElement rate = taxes1.GetComplexElement("Rate");


ComplexElement baseAmount = taxes1.GetComplexElement("BaseAmount");


ComplexElement appliedAmount = taxes1.GetComplexElement("AppliedAmount");


ComplexElement remarks = taxes1.GetComplexElement("Remarks");

ComplexElementArrayItem taxes2 = taxes[2];
taxes2.GetValue("TypeId");
taxes2.GetValue("TypeDescription");
taxes2.GetValue("Amount");
taxes2.GetValue("Rate");
taxes2.GetValue("BaseAmount");

ComplexElement appliedAmount = taxes2.GetComplexElement("AppliedAmount");


ComplexElement remarks = taxes2.GetComplexElement("Remarks");