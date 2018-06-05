ComplexElement customerDetails = response.getComplexElement("CustomerDetails");


local customerDetails = customerDetails.CustomerDetails
print(customerDetails.EmailAddress)
print(customerDetails.AlternativeEmailAddress)
print(customerDetails.IPAddress)
print(customerDetails.AccountID)
print(customerDetails.AccountCreatedAt)
print(customerDetails.AccountPreviousActivity)
print(customerDetails.AccountHasCredentials)
print(customerDetails.DeviceType)
print(customerDetails.DeviceFingerPrint)
print(customerDetails.BrowserLanguage)
print(customerDetails.HttpUserAgent)

