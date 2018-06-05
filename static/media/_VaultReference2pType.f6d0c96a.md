using System;
using NpsSDK;

ComplexElement VaultReference2p = response.GetComplexElement("VaultReference2p");


ComplexElement vaultReference2p = VaultReference2p.GetComplexElement("VaultReference2p");
vaultReference2p.GetValue("PaymentMethodId");
vaultReference2p.GetValue("CustomerId");

