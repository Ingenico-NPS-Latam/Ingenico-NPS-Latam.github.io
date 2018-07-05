using System;
using NpsSDK;

ComplexElement Taxes = response.GetComplexElement("Taxes");


ComplexElement taxes = Taxes.GetComplexElement("Taxes");
taxes.GetValue("TypeId");
taxes.GetValue("Amount");
taxes.GetValue("Rate");
taxes.GetValue("BaseAmount");

