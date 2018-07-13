RootElement data = new RootElement();


ComplexElement InstallmentsOptions = new ComplexElement();
InstallmentsOptions.Add("NumPayments", "12");
InstallmentsOptions.Add("InstallmentAmount", "10");
InstallmentsOptions.Add("InterestRate", "1");

data.Add("InstallmentsOptions", InstallmentsOptions);
