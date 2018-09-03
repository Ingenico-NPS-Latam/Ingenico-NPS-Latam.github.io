import npsSdk

let nps = Nps(environment: NPSSANDBOX)!
nps.merchantId = "__YOUR_NPS_MERCHANT_ID__"
nps.clientSession = "__YOUR_NPS_CLIENT_SESSION__"

let card = NpsCardDetails()

card.number = "4507990000000010";
card.holderName = "JOHN DOE";
card.securityCode = "123";
card.expirationDate = "1909";

nps.createPaymentMethodToken(card, billingDetails: nil, methodResponse: {( methodResponse: NpsCreatePaymentMethodTokenResponse?, error: Error?) -> Void in
    if error == nil{
        print(methodResponse?.responseExtended as Any)
    }
})