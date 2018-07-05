ComplexElement installmentsOptions = response.getComplexElement("InstallmentsOptions");


local installmentsOptions = installmentsOptions.InstallmentsOptions
print(installmentsOptions.NumPayments)
print(installmentsOptions.InstallmentAmount)
print(installmentsOptions.InterestRate)

