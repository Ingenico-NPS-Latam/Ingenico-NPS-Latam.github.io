import npsSdk

let nps = Nps(environment: NPSSANDBOX)!
nps.merchantId = "__YOUR_NPS_MERCHANT_ID__"
nps.clientSession = "__YOUR_NPS_CLIENT_SESSION__"

let wallet = NpsWallet()

wallet.typeId = "2";
wallet.key = "d084703513e87cd1540a114cd7317e6642eca04e";
wallet.orderId = "1efed583-1824-436a-869f-286ebdb22ae9";

nps.createPaymentMethodToken(nil, billingDetails: nil, wallet: wallet methodResponse: {( methodResponse: NpsCreatePaymentMethodTokenResponse?, error: Error?) -> Void in
    if error == nil{
        print(methodResponse?.responseExtended as Any)
    }
})