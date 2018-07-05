using System;
using NpsSDK;

ComplexElement OrderDetails = response.GetComplexElement("OrderDetails");


ComplexElementArray orderDetails = OrderDetails.GetComplexElementArray("OrderDetails");

ComplexElementArrayItem orderDetails1 = orderDetails[1];
orderDetails1.GetValue("Quantity");
orderDetails1.GetValue("UnitPrice");
orderDetails1.GetValue("Description");
orderDetails1.GetValue("Type");
orderDetails1.GetValue("SkuCode");
orderDetails1.GetValue("ManufacturerPartNumber");
orderDetails1.GetValue("Risk");


ComplexElementArrayItem orderDetails2 = orderDetails[2];
orderDetails2.GetValue("Quantity");
orderDetails2.GetValue("UnitPrice");
orderDetails2.GetValue("Description");
orderDetails2.GetValue("Type");
orderDetails2.GetValue("SkuCode");
orderDetails2.GetValue("ManufacturerPartNumber");
orderDetails2.GetValue("Risk");


