import npsSdk

let nps = Nps(environment: NPSSANDBOX)!
nps.merchantId = "__YOUR_NPS_MERCHANT_ID__"
nps.clientSession = "__YOUR_NPS_CLIENT_SESSION__"

nps.retrievePaymentMethodToken("KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM", methodResponse: {( methodResponse: NpsRetrievePaymentMethodTokenResponse?, error: Error?) -> Void in
    if error == nil{
        print(methodResponse?.responseExtended as Any)
    }
})

