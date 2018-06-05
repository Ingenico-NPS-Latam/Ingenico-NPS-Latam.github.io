import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement cardInputDetails = response.getComplexElement("CardInputDetails");

cardInputDetails.getValue("Number");
cardInputDetails.getValue("ExpirationDate");
cardInputDetails.getValue("SecurityCode");
cardInputDetails.getValue("HolderName");
