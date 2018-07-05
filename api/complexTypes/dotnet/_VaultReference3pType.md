using System;
using NpsSDK;

ComplexElement VaultReference3p = response.GetComplexElement("VaultReference3p");


ComplexElement vaultReference3p = VaultReference3p.GetComplexElement("VaultReference3p");
vaultReference3p.GetValue("CustomerId");

