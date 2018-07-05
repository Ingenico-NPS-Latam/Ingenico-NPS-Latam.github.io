ComplexElement orderDetails = response.getComplexElement("OrderDetails");


local orderDetails = orderDetails.OrderDetails

localorderDetails1 := orderDetails[1]
print(orderDetails1.Quantity)
print(orderDetails1.UnitPrice)
print(orderDetails1.Description)
print(orderDetails1.Type)
print(orderDetails1.SkuCode)
print(orderDetails1.ManufacturerPartNumber)
print(orderDetails1.Risk)


localorderDetails2 := orderDetails[2]
print(orderDetails2.Quantity)
print(orderDetails2.UnitPrice)
print(orderDetails2.Description)
print(orderDetails2.Type)
print(orderDetails2.SkuCode)
print(orderDetails2.ManufacturerPartNumber)
print(orderDetails2.Risk)


