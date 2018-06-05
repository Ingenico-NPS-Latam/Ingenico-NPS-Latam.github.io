import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement customerDetails = response.getComplexElement("CustomerDetails");


ComplexElement customerDetails = customerDetails.getComplexElement("CustomerDetails");
customerDetails.getValue("EmailAddress");
customerDetails.getValue("AlternativeEmailAddress");
customerDetails.getValue("IPAddress");
customerDetails.getValue("AccountID");
customerDetails.getValue("AccountCreatedAt");
customerDetails.getValue("AccountPreviousActivity");
customerDetails.getValue("AccountHasCredentials");
customerDetails.getValue("DeviceType");
customerDetails.getValue("DeviceFingerPrint");
customerDetails.getValue("BrowserLanguage");
customerDetails.getValue("HttpUserAgent");

