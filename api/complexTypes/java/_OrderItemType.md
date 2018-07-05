import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement orderItem = response.getComplexElement("OrderItem");


ComplexElement orderItem = orderItem.getComplexElement("OrderItem");
orderItem.getValue("Quantity");
orderItem.getValue("UnitPrice");
orderItem.getValue("Description");
orderItem.getValue("Type");
orderItem.getValue("SkuCode");
orderItem.getValue("ManufacturerPartNumber");
orderItem.getValue("Risk");

