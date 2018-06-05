#import "Nps.h"

Nps *nps = [[Nps alloc]initWithEnvironment:NPSSANDBOX];
nps.merchantId = @"__YOUR_NPS_MERCHANT_ID__";
nps.clientSession = @"__YOUR_NPS_CLIENT_SESSION__";

[nps getInstallmentsOptions:@"100"
                    product:@"14"
                   currency:@"152"
                    country:@"CHL"
                numPayments:@"2"
         paymentMethodToken:@"kkvKuOfD2bNKXCBYDkunIRqImvNFNxB3"
             methodResponse:^(NpsGetInstallmentsOptionsResponse *methodResponse, NSError *error) {
                     if (!error){
                         NSLog(@"%@", [methodResponse responseCod]);
                         for (Installments *inst in [methodResponse installments]){
                             NSLog(@"%@", [inst installmentAmount]);
                             NSLog(@"%@", [inst interestRate]);
                             NSLog(@"%@", [inst numPayments]);
                         }
                     }
                 }];;