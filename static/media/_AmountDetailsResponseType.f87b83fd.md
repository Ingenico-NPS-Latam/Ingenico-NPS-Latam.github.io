import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.amountDetailsResponseType.md(data);


ComplexElement amountDetailResponse = response.getComplexElement("AmountDetailResponse");
amountDetailResponse.getValue("Tip");
amountDetailResponse.getValue("Discount");

List<ComplexElementArrayItem> taxes = AmountDetailResponse.getComplexElementArray('Taxes');

ComplexElementArrayItem taxes1 = taxes.getValue(1);
taxes1.getValue("TypeId");
taxes1.getValue("Amount");
taxes1.getValue("Rate");
taxes1.getValue("BaseAmount");


ComplexElementArrayItem taxes2 = taxes.getValue(2);
taxes2.getValue("TypeId");
taxes2.getValue("Amount");
taxes2.getValue("Rate");
taxes2.getValue("BaseAmount");



