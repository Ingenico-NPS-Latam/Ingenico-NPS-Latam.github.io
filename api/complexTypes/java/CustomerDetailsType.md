RootElement data = new RootElement();


ComplexElement CustomerDetails = new ComplexElement();
CustomerDetails.add("EmailAddress", "jdoe@email.com");
CustomerDetails.add("AlternativeEmailAddress", "Jdoe79@email.com");
CustomerDetails.add("IPAddress", "192.168.158.190");
CustomerDetails.add("AccountID", "Jdoe78");
CustomerDetails.add("AccountCreatedAt", "2010-10-23");
CustomerDetails.add("AccountPreviousActivity", "1");
CustomerDetails.add("AccountHasCredentials", "1");
CustomerDetails.add("DeviceType", "1");
CustomerDetails.add("DeviceFingerPrint", "KJhKHKJgh7777kgh");
CustomerDetails.add("BrowserLanguage", "ES");
CustomerDetails.add("HttpUserAgent", "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0");

data.add("CustomerDetails", CustomerDetails);
