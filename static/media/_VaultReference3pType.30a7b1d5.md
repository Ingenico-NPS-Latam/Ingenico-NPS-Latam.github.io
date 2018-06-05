import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement vaultReference3p = response.getComplexElement("VaultReference3p");


ComplexElement vaultReference3p = vaultReference3p.getComplexElement("VaultReference3p");
vaultReference3p.getValue("CustomerId");

