using System;
using NpsSDK;

ComplexElement OrderItem = response.GetComplexElement("OrderItem");


ComplexElement orderItem = OrderItem.GetComplexElement("OrderItem");
orderItem.GetValue("Quantity");
orderItem.GetValue("UnitPrice");
orderItem.GetValue("Description");
orderItem.GetValue("Type");
orderItem.GetValue("SkuCode");
orderItem.GetValue("ManufacturerPartNumber");
orderItem.GetValue("Risk");

