nps.recachePaymentMethodToken("kWRZGcAxy5D7MoB6BDACugHYrlFzP9Eg",
            cardSecurityCode: "123",
              billingDetails: billing,
              methodResponse: {( methodResponse: NpsRecachePaymentMethodTokenResponse?, error: Error?) -> Void in
                    if error == nil{
                        print(methodResponse?.responseCod as Any)
                        print(methodResponse?.responseMsg as Any)
                        print(methodResponse?.merchandId as Any)
                        print(methodResponse?.paymentMethodToken as Any)
                        print(methodResponse?.product as Any)

                        let cardDetails = methodResponse?.product
                        print(cardDetails.expirationDate as Any)
                        print(cardDetails.expirationYear as Any)
                        print(cardDetails.expirationMonth as Any)
                        print(cardDetails.holderName as Any)
                        print(cardDetails.IIN as Any)
                        print(cardDetails.last4 as Any)
                        print(cardDetails.numberLength as Any)
                        print(cardDetails.maskedNumber as Any)
                        print(cardDetails.maskedNumberAlternative as Any)

                        print(methodResponse?.alreadyUsed as Any)
                        print(methodResponse?.createdAt as Any)
                        print(methodResponse?.updateAt as Any)
                    }
})
