using System;
using NpsSDK;

ComplexElement CustomerDetails = response.GetComplexElement("CustomerDetails");


ComplexElement customerDetails = CustomerDetails.GetComplexElement("CustomerDetails");
customerDetails.GetValue("EmailAddress");
customerDetails.GetValue("AlternativeEmailAddress");
customerDetails.GetValue("IPAddress");
customerDetails.GetValue("AccountID");
customerDetails.GetValue("AccountCreatedAt");
customerDetails.GetValue("AccountPreviousActivity");
customerDetails.GetValue("AccountHasCredentials");
customerDetails.GetValue("DeviceType");
customerDetails.GetValue("DeviceFingerPrint");
customerDetails.GetValue("BrowserLanguage");
customerDetails.GetValue("HttpUserAgent");

