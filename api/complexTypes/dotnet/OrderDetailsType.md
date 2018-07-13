RootElement data = new RootElement();


ComplexElementArray OrderItems = new ComplexElementArray();

ComplexElementArrayItem OrderItems1 = new ComplexElementArrayItem();
OrderItems1.Add("Quantity", "10");
OrderItems1.Add("UnitPrice", "10050");
OrderItems1.Add("Description", "Blue pencil");
OrderItems1.Add("Type", "1002");
OrderItems1.Add("SkuCode", "SO-4587885545");
OrderItems1.Add("ManufacturerPartNumber", "CN-0N2828421-3AD-02CD");
OrderItems1.Add("Risk", "H");

OrderItems.Add(OrderItems1);

ComplexElementArrayItem OrderItems2 = new ComplexElementArrayItem();
OrderItems2.Add("Quantity", "10");
OrderItems2.Add("UnitPrice", "10050");
OrderItems2.Add("Description", "Blue pencil");
OrderItems2.Add("Type", "1002");
OrderItems2.Add("SkuCode", "SO-4587885545");
OrderItems2.Add("ManufacturerPartNumber", "CN-0N2828421-3AD-02CD");
OrderItems2.Add("Risk", "H");

OrderItems.Add(OrderItems2);

data.Add("OrderItems", OrderItems);
