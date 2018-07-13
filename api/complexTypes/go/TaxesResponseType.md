Taxes := nps.NewTaxesResponseStruct()

Taxes := nps.NewTaxesRequestStruct()
Taxes.TypeId = "601"
Taxes.TypeDescription = "IVA (Ley 19210)"
Taxes.Amount = "10000"
Taxes.Rate = "1050"
Taxes.BaseAmount = "10000"
Taxes.AppliedAmount = "8500"
Taxes.Remarks = "IVA Ley 19210"

Taxes.Taxes = Taxes
