import npsSdk

let nps = Nps(environment: NPSSANDBOX)!
nps.merchantId = "__YOUR_NPS_MERCHANT_ID__"
nps.clientSession = "__YOUR_NPS_CLIENT_SESSION__"

nps.recachePaymentMethodToken("kWRZGcAxy5D7MoB6BDACugHYrlFzP9Eg", 
            cardSecurityCode: "123", 
              billingDetails: nil,
              methodResponse: {( methodResponse: NpsRecachePaymentMethodTokenResponse?, error: Error?) -> Void in
                    if error == nil{
                        print(methodResponse?.responseCod as Any)
                    }
})