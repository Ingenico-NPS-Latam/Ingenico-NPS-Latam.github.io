import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement installmentsOptions = response.getComplexElement("InstallmentsOptions");


ComplexElement installmentsOptions = installmentsOptions.getComplexElement("InstallmentsOptions");
installmentsOptions.getValue("NumPayments");
installmentsOptions.getValue("InstallmentAmount");
installmentsOptions.getValue("InterestRate");

