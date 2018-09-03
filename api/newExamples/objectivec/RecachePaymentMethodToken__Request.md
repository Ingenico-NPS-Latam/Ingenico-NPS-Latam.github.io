#import "Nps.h"

Nps *nps = [[Nps alloc]initWithEnvironment:NPSSANDBOX];
nps.merchantId = @"__YOUR_NPS_MERCHANT_ID__";
nps.clientSession = @"__YOUR_NPS_CLIENT_SESSION__";

[nps recachePaymentMethodToken:@"kWRZGcAxy5D7MoB6BDACugHYrlFzP9Eg"
              cardSecurityCode:@"123"
                billingDetails:nil
                methodResponse:^(NpsRecachePaymentMethodTokenResponse *methodResponse, NSError *error) {
                    if (!error){
                        NSLog(@"%@", [methodResponse responseCod]);
                    }
}];
