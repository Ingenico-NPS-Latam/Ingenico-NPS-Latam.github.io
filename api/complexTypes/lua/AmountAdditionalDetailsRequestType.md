AmountAdditionalDetails = {}

AmountAdditionalDetails.Tip = "500"
AmountAdditionalDetails.Discount = "10000"

Taxes = {}

Taxes1 = {}
Taxes1.TypeId = "500"
Taxes1.Amount = "10000"
Taxes1.Rate = "2100"
Taxes1.BaseAmount = "10000"

Taxes[#Taxes+1] = Taxes1

Taxes2 = {}
Taxes2.TypeId = "500"
Taxes2.Amount = "10000"
Taxes2.Rate = "2100"
Taxes2.BaseAmount = "10000"

Taxes[#Taxes+1] = Taxes2

AmountAdditionalDetails.Taxes = Taxes
