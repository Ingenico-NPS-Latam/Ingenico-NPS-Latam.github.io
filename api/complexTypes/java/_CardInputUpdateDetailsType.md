import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement cardInputUpdateDetails = response.getComplexElement("CardInputUpdateDetails");

cardInputUpdateDetails.getValue("ExpirationDate");
cardInputUpdateDetails.getValue("HolderName");
