#import "Nps.h"

Nps *nps = [[Nps alloc]initWithEnvironment:NPSSANDBOX];
nps.merchantId = @"__YOUR_NPS_MERCHANT_ID__";
nps.clientSession = @"__YOUR_NPS_CLIENT_SESSION__";

[nps getIINDetails:@"424242"
 methodResponse:^(NpsGetIINDetailsResponse *methodResponse, NSError *error) {
    if(!error){
        NSLog(@"%@", [methodResponse responseCod]);
    }
}];