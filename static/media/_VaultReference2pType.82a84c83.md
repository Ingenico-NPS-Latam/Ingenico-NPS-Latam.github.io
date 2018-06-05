import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement vaultReference2p = response.getComplexElement("VaultReference2p");


ComplexElement vaultReference2p = vaultReference2p.getComplexElement("VaultReference2p");
vaultReference2p.getValue("PaymentMethodId");
vaultReference2p.getValue("CustomerId");

