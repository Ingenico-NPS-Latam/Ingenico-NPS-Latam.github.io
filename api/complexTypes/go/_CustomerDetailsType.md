ComplexElement customerDetails = response.getComplexElement("CustomerDetails");


customerDetails := customerDetails.CustomerDetails
fmt.Printf(customerDetails.EmailAddress)
fmt.Printf(customerDetails.AlternativeEmailAddress)
fmt.Printf(customerDetails.IPAddress)
fmt.Printf(customerDetails.AccountID)
fmt.Printf(customerDetails.AccountCreatedAt)
fmt.Printf(customerDetails.AccountPreviousActivity)
fmt.Printf(customerDetails.AccountHasCredentials)
fmt.Printf(customerDetails.DeviceType)
fmt.Printf(customerDetails.DeviceFingerPrint)
fmt.Printf(customerDetails.BrowserLanguage)
fmt.Printf(customerDetails.HttpUserAgent)

