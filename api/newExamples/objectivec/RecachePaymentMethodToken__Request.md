#import "Nps.h"

Nps *nps = [[Nps alloc]initWithEnvironment:NPSSANDBOX];
nps.merchantId = @"__YOUR_NPS_MERCHANT_ID__";
nps.clientSession = @"__YOUR_NPS_CLIENT_SESSION__";


NpsBilling *billing = [[NpsBilling alloc]init];

billing.pspPerson.firstName = @"JOHN";
billing.pspPerson.lastName = @"Smith";
billing.pspPerson.dateOfBirth = @"1987-01-01";
billing.pspPerson.gender = @"M";
billing.pspPerson.nationality = @"ARG";
billing.pspPerson.idType = @"DNI";
billing.pspPerson.idNumber = @"32123123";
billing.pspPerson.phoneNumber1 = @"4123-1234";
billing.pspPerson.phoneNumber2 = @"4123-5678";

billing.pspAddress.additionalInfo = @"JOHN";
billing.pspAddress.city = @"Smith";
billing.pspAddress.stateProvince = @"Buenos Aires";
billing.pspAddress.country = @"M";
billing.pspAddress.zipCode = @"ARG";
billing.pspAddress.street = @"DNI";
billing.pspAddress.houseNumber = @"32123123";

[nps recachePaymentMethodToken:@"kWRZGcAxy5D7MoB6BDACugHYrlFzP9Eg"
              cardSecurityCode:@"123"
                billingDetails:billingDetailss
                methodResponse:^(NpsRecachePaymentMethodTokenResponse *methodResponse, NSError *error) {
                    if (!error){
                        NSLog(@"%@", [methodResponse responseCod]);
                    }
}];
