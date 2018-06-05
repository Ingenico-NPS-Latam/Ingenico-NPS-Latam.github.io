nps.getInstallmentsOptions("100",
                    product:@"14",
                   currency:@"152",
                    country:@"CHL",
                numPayments:@"2",
         paymentMethodToken:@"kkvKuOfD2bNKXCBYDkunIRqImvNFNxB3",
              methodResponse: {( methodResponse: NpsGetInstallmentsOptionsResponse?, error: Error?) -> Void in
                    if error == nil{
                         print(methodResponse?.responseCod as Any)
                         print(methodResponse?.responseMsg as Any)
                         print(methodResponse?.merchandId as Any)
                         print(methodResponse?.amount as Any)
                         print(methodResponse?.product as Any)
                         print(methodResponse?.currency as Any)
                         print(methodResponse?.country as Any)
                         print(methodResponse?.numPayments as Any)

                         for inst in methodResponse?.installments{
                            print(inst.numPayments)
                            print(inst.installmentAmount)
                         }

                         print(methodResponse?.posDateTime as Any)
                     }
})




