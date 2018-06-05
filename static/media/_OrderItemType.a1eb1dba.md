ComplexElement orderItem = response.getComplexElement("OrderItem");


local orderItem = orderItem.OrderItem
print(orderItem.Quantity)
print(orderItem.UnitPrice)
print(orderItem.Description)
print(orderItem.Type)
print(orderItem.SkuCode)
print(orderItem.ManufacturerPartNumber)
print(orderItem.Risk)

