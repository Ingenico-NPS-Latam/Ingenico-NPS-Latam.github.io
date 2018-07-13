RootElement data = new RootElement();


ComplexElement CustomerDetails = new ComplexElement();
CustomerDetails.Add("EmailAddress", "jdoe@email.com");
CustomerDetails.Add("AlternativeEmailAddress", "Jdoe79@email.com");
CustomerDetails.Add("IPAddress", "192.168.158.190");
CustomerDetails.Add("AccountID", "Jdoe78");
CustomerDetails.Add("AccountCreatedAt", "2010-10-23");
CustomerDetails.Add("AccountPreviousActivity", "1");
CustomerDetails.Add("AccountHasCredentials", "1");
CustomerDetails.Add("DeviceType", "1");
CustomerDetails.Add("DeviceFingerPrint", "KJhKHKJgh7777kgh");
CustomerDetails.Add("BrowserLanguage", "ES");
CustomerDetails.Add("HttpUserAgent", "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0");

data.Add("CustomerDetails", CustomerDetails);
