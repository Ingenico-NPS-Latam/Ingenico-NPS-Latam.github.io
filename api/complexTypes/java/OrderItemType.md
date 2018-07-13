RootElement data = new RootElement();


ComplexElement OrderItem = new ComplexElement();
OrderItem.add("Quantity", "10");
OrderItem.add("UnitPrice", "10050");
OrderItem.add("Description", "Blue pencil");
OrderItem.add("Type", "1002");
OrderItem.add("SkuCode", "SO-4587885545");
OrderItem.add("ManufacturerPartNumber", "CN-0N2828421-3AD-02CD");
OrderItem.add("Risk", "H");

data.add("OrderItem", OrderItem);
