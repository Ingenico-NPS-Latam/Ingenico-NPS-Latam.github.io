using System;
using NpsSDK;

ComplexElement VerificationServicesResult = response.GetComplexElement("VerificationServicesResult");

verificationServicesResult.GetValue("ResultCodeCardSecurityCode");
verificationServicesResult.GetValue("ResultCodeBillingAddress");
verificationServicesResult.GetValue("ResultCodeBillingAddressZipCode");
verificationServicesResult.GetValue("ResultCodeBillingPersonIDType");
verificationServicesResult.GetValue("ResultCodeBillingPersonIDNumber");
verificationServicesResult.GetValue("ResultCodeBillingPersonDateOfBirth");
verificationServicesResult.GetValue("ResultCodeBillingPersonName");
verificationServicesResult.GetValue("ResultCodeBillingPersonPhoneNumber1");
verificationServicesResult.GetValue("ResultCodeCustomerEmailAddress");
