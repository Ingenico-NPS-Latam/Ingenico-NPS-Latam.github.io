import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement taxes = response.getComplexElement("Taxes");


ComplexElement taxes = taxes.getComplexElement("Taxes");
taxes.getValue("TypeId");
taxes.getValue("Amount");
taxes.getValue("Rate");
taxes.getValue("BaseAmount");

