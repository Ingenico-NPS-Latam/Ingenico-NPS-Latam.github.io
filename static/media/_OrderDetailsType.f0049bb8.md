import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement orderDetails = response.getComplexElement("OrderDetails");


List<ComplexElementArrayItem> orderDetails = orderDetails.getComplexElementArray('OrderDetails');

ComplexElementArrayItem orderDetails1 = orderDetails.getValue(1);
orderDetails1.getValue("Quantity");
orderDetails1.getValue("UnitPrice");
orderDetails1.getValue("Description");
orderDetails1.getValue("Type");
orderDetails1.getValue("SkuCode");
orderDetails1.getValue("ManufacturerPartNumber");
orderDetails1.getValue("Risk");


ComplexElementArrayItem orderDetails2 = orderDetails.getValue(2);
orderDetails2.getValue("Quantity");
orderDetails2.getValue("UnitPrice");
orderDetails2.getValue("Description");
orderDetails2.getValue("Type");
orderDetails2.getValue("SkuCode");
orderDetails2.getValue("ManufacturerPartNumber");
orderDetails2.getValue("Risk");


