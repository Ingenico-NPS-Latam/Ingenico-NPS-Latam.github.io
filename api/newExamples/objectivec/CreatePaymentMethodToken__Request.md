#import "Nps.h"

Nps *nps = [[Nps alloc]initWithEnvironment:NPSSANDBOX];
nps.merchantId = @"__YOUR_NPS_MERCHANT_ID__";
nps.clientSession = @"__YOUR_NPS_CLIENT_SESSION__";

NpsCardDetails *card = [[NpsCardDetails alloc]init];

card.number = @"4507990000000010";
card.holderName = @"JOHN DOE";
card.securityCode = @"123";
card.expirationDate = @"1909";

[nps createPaymentMethodToken:card
              billingDetails:nil
              methodResponse:^(NpsCreatePaymentMethodTokenResponse* methodResponse, NSError *error) {
                if(!error){
                    NSLog(@"%@", [methodResponse responseCod]);
                }
}];