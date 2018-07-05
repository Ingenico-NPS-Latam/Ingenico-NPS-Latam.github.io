import npsSdk

let nps = Nps(environment: NPSSANDBOX)!
nps.merchantId = "__YOUR_NPS_MERCHANT_ID__"
nps.clientSession = "__YOUR_NPS_CLIENT_SESSION__"

nps.getIINDetails("424242",
    methodResponse:{( methodResponse: NpsGetIINDetailsResponse?, error: Error?) -> Void in
        if error == nil{
            print(methodResponse?.responseCod as Any)
        }
    })
