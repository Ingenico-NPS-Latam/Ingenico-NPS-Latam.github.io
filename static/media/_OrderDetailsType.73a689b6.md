ComplexElement orderDetails = response.getComplexElement("OrderDetails");


orderDetails := orderDetails.OrderDetails

orderDetails1 := orderDetails.Items[1];
fmt.Printf(orderDetails1.Quantity)
fmt.Printf(orderDetails1.UnitPrice)
fmt.Printf(orderDetails1.Description)
fmt.Printf(orderDetails1.Type)
fmt.Printf(orderDetails1.SkuCode)
fmt.Printf(orderDetails1.ManufacturerPartNumber)
fmt.Printf(orderDetails1.Risk)


orderDetails2 := orderDetails.Items[2];
fmt.Printf(orderDetails2.Quantity)
fmt.Printf(orderDetails2.UnitPrice)
fmt.Printf(orderDetails2.Description)
fmt.Printf(orderDetails2.Type)
fmt.Printf(orderDetails2.SkuCode)
fmt.Printf(orderDetails2.ManufacturerPartNumber)
fmt.Printf(orderDetails2.Risk)


