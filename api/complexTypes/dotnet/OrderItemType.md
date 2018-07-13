RootElement data = new RootElement();


ComplexElement OrderItem = new ComplexElement();
OrderItem.Add("Quantity", "10");
OrderItem.Add("UnitPrice", "10050");
OrderItem.Add("Description", "Blue pencil");
OrderItem.Add("Type", "1002");
OrderItem.Add("SkuCode", "SO-4587885545");
OrderItem.Add("ManufacturerPartNumber", "CN-0N2828421-3AD-02CD");
OrderItem.Add("Risk", "H");

data.Add("OrderItem", OrderItem);
