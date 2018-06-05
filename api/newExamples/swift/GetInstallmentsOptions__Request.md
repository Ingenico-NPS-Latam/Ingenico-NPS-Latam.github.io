import npsSdk

let nps = Nps(environment: NPSSANDBOX)!
nps.merchantId = "__YOUR_NPS_MERCHANT_ID__"
nps.clientSession = "__YOUR_NPS_CLIENT_SESSION__"

nps.getInstallmentsOptions("100", 
                    product:@"14",
                   currency:@"152",
                    country:@"CHL",
                numPayments:@"2",
         paymentMethodToken:@"kkvKuOfD2bNKXCBYDkunIRqImvNFNxB3",
              methodResponse: {( methodResponse: NpsGetInstallmentsOptionsResponse?, error: Error?) -> Void in
                    if error == nil{
                         print(methodResponse?.responseCod as Any)
                         for inst in methodResponse?.installments{
                            print(inst.installmentAmount)
                            print(inst.interestRate)
                            print(inst.numPayments)
                         }
                     }
})