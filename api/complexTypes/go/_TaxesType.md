ComplexElement taxes = response.getComplexElement("Taxes");


taxes := taxes.Taxes
fmt.Printf(taxes.TypeId)
fmt.Printf(taxes.Amount)
fmt.Printf(taxes.Rate)
fmt.Printf(taxes.BaseAmount)

