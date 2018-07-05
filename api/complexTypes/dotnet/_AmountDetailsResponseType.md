using System;
using NpsSDK;

RootElement response = npsSdk.AmountDetailsResponseType.md(data);


ComplexElement amountDetailResponse = response.GetComplexElement("AmountDetailResponse");
amountDetailResponse.GetValue("Tip");
amountDetailResponse.GetValue("Discount");

ComplexElementArray taxes = AmountDetailResponse.GetComplexElementArray("Taxes");

ComplexElementArrayItem taxes1 = taxes[1];
taxes1.GetValue("TypeId");
taxes1.GetValue("Amount");
taxes1.GetValue("Rate");
taxes1.GetValue("BaseAmount");


ComplexElementArrayItem taxes2 = taxes[2];
taxes2.GetValue("TypeId");
taxes2.GetValue("Amount");
taxes2.GetValue("Rate");
taxes2.GetValue("BaseAmount");



