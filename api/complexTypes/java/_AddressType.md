import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement address = response.getComplexElement("Address");

address.getValue("AdditionalInfo");
address.getValue("City");
address.getValue("Country");
address.getValue("HouseNumber");
address.getValue("StateProvince");
address.getValue("Street");
address.getValue("ZipCode");
