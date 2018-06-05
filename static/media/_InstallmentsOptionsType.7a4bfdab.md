using System;
using NpsSDK;

ComplexElement InstallmentsOptions = response.GetComplexElement("InstallmentsOptions");


ComplexElement installmentsOptions = InstallmentsOptions.GetComplexElement("InstallmentsOptions");
installmentsOptions.GetValue("NumPayments");
installmentsOptions.GetValue("InstallmentAmount");
installmentsOptions.GetValue("InterestRate");

