RootElement data = new RootElement();


ComplexElementArray OrderItems = new ComplexElementArray();

ComplexElementArrayItem OrderItems1 = new ComplexElementArrayItem();
OrderItems1.add("Quantity", "10");
OrderItems1.add("UnitPrice", "10050");
OrderItems1.add("Description", "Blue pencil");
OrderItems1.add("Type", "1002");
OrderItems1.add("SkuCode", "SO-4587885545");
OrderItems1.add("ManufacturerPartNumber", "CN-0N2828421-3AD-02CD");
OrderItems1.add("Risk", "H");

OrderItems.add(OrderItems1);

ComplexElementArrayItem OrderItems2 = new ComplexElementArrayItem();
OrderItems2.add("Quantity", "10");
OrderItems2.add("UnitPrice", "10050");
OrderItems2.add("Description", "Blue pencil");
OrderItems2.add("Type", "1002");
OrderItems2.add("SkuCode", "SO-4587885545");
OrderItems2.add("ManufacturerPartNumber", "CN-0N2828421-3AD-02CD");
OrderItems2.add("Risk", "H");

OrderItems.add(OrderItems2);

data.add("OrderItems", OrderItems);
