ComplexElement taxes = response.getComplexElement("Taxes");


local taxes = taxes.Taxes
print(taxes.TypeId)
print(taxes.Amount)
print(taxes.Rate)
print(taxes.BaseAmount)

