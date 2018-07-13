RootElement data = new RootElement();


ComplexElement InstallmentsOptions = new ComplexElement();
InstallmentsOptions.add("NumPayments", "12");
InstallmentsOptions.add("InstallmentAmount", "10");
InstallmentsOptions.add("InterestRate", "1");

data.add("InstallmentsOptions", InstallmentsOptions);
