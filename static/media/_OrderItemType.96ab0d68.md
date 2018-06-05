ComplexElement orderItem = response.getComplexElement("OrderItem");


orderItem := orderItem.OrderItem
fmt.Printf(orderItem.Quantity)
fmt.Printf(orderItem.UnitPrice)
fmt.Printf(orderItem.Description)
fmt.Printf(orderItem.Type)
fmt.Printf(orderItem.SkuCode)
fmt.Printf(orderItem.ManufacturerPartNumber)
fmt.Printf(orderItem.Risk)

