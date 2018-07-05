ComplexElement installmentsOptions = response.getComplexElement("InstallmentsOptions");


installmentsOptions := installmentsOptions.InstallmentsOptions
fmt.Printf(installmentsOptions.NumPayments)
fmt.Printf(installmentsOptions.InstallmentAmount)
fmt.Printf(installmentsOptions.InterestRate)

