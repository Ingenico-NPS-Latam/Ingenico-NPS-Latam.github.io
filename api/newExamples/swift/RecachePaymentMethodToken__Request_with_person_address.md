import npsSdk

let nps = Nps(environment: NPSSANDBOX)!
nps.merchantId = "__YOUR_NPS_MERCHANT_ID__"
nps.clientSession = "__YOUR_NPS_CLIENT_SESSION__"

let billing = NpsBilling()

billing.pspPerson.firstName = "JOHN";
billing.pspPerson.lastName = "Smith";
billing.pspPerson.dateOfBirth = "1987-01-01";
billing.pspPerson.gender = "M";
billing.pspPerson.nationality = "ARG";
billing.pspPerson.idType = "200";
billing.pspPerson.idNumber = "95665091";
billing.pspPerson.phoneNumber1 = "4123-1234";
billing.pspPerson.phoneNumber2 = "4123-5678";

billing.pspAddress.additionalInfo = "JOHN";
billing.pspAddress.city = "Buenos Aires";
billing.pspAddress.stateProvince = "CABA";
billing.pspAddress.country = "ARG";
billing.pspAddress.zipCode = "1425";
billing.pspAddress.street = "suipacha";
billing.pspAddress.houseNumber = "32123123";

nps.recachePaymentMethodToken("kWRZGcAxy5D7MoB6BDACugHYrlFzP9Eg", 
            cardSecurityCode: "123", 
              billingDetails: billing,
              methodResponse: {( methodResponse: NpsRecachePaymentMethodTokenResponse?, error: Error?) -> Void in
                    if error == nil{
                        print(methodResponse?.responseCod as Any)
                    }
})