AmountDetail := nps.NewAmountDetailStruct()

AmountDetail.Tip = "20000"
AmountDetail.Discount = "11000"

Taxes := nps.NewArrayOf_TaxesRequestStruct()

Taxes1 := nps.NewTaxesRequestStruct()
Taxes1.TypeId = "500"
Taxes1.Amount = "10000"
Taxes1.Rate = "2100"
Taxes1.BaseAmount = "10000"

Taxes.Items = append(Taxes.Items, Taxes1)
Taxes2 := nps.NewTaxesRequestStruct()
Taxes2.TypeId = "500"
Taxes2.Amount = "10000"
Taxes2.Rate = "2100"
Taxes2.BaseAmount = "10000"

Taxes.Items = append(Taxes.Items, Taxes2)

AmountDetail.Taxes = Taxes
