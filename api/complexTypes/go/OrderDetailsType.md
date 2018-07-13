OrderDetails := nps.NewOrderDetailsStruct()

OrderItems := nps.NewArrayOf_OrderItemsStruct()
OrderItems.Items = make([]*nps.NewOrderItemsStruct(), 0)

OrderItems1 := nps.NewOrderItemsStruct()
OrderItems1.Quantity = "10"
OrderItems1.UnitPrice = "10050"
OrderItems1.Description = "Blue pencil"
OrderItems1.Type = "1002"
OrderItems1.SkuCode = "SO-4587885545"
OrderItems1.ManufacturerPartNumber = "CN-0N2828421-3AD-02CD"
OrderItems1.Risk = "H"
OrderItems.Items = append(OrderItems.Items, OrderItems1)

OrderItems2 := nps.NewOrderItemsStruct()
OrderItems2.Quantity = "10"
OrderItems2.UnitPrice = "10050"
OrderItems2.Description = "Blue pencil"
OrderItems2.Type = "1002"
OrderItems2.SkuCode = "SO-4587885545"
OrderItems2.ManufacturerPartNumber = "CN-0N2828421-3AD-02CD"
OrderItems2.Risk = "H"
OrderItems.Items = append(OrderItems.Items, OrderItems2)

