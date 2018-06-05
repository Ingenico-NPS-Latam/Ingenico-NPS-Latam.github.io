import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement verificationServicesResult = response.getComplexElement("VerificationServicesResult");

verificationServicesResult.getValue("ResultCodeCardSecurityCode");
verificationServicesResult.getValue("ResultCodeBillingAddress");
verificationServicesResult.getValue("ResultCodeBillingAddressZipCode");
verificationServicesResult.getValue("ResultCodeBillingPersonIDType");
verificationServicesResult.getValue("ResultCodeBillingPersonIDNumber");
verificationServicesResult.getValue("ResultCodeBillingPersonDateOfBirth");
verificationServicesResult.getValue("ResultCodeBillingPersonName");
verificationServicesResult.getValue("ResultCodeBillingPersonPhoneNumber1");
verificationServicesResult.getValue("ResultCodeCustomerEmailAddress");
