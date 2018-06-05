[nps getInstallmentsOptions:@"100"
                    product:@"14"
                   currency:@"152"
                    country:@"CHL"
                numPayments:@"2"
         paymentMethodToken:@"kkvKuOfD2bNKXCBYDkunIRqImvNFNxB3"
             methodResponse:^(NpsGetInstallmentsOptionsResponse *methodResponse, NSError *error) {
                     if (!error){
                         NSLog(@"%@", [methodResponse responseCod]);
                         NSLog(@"%@", [methodResponse responseMsg]);
                         NSLog(@"%@", [methodResponse merchandId]);
                         NSLog(@"%@", [methodResponse amount]);
                         NSLog(@"%@", [methodResponse product]);
                         NSLog(@"%@", [methodResponse currency]);
                         NSLog(@"%@", [methodResponse country]);
                         NSLog(@"%@", [methodResponse numPayments]);

                         for (Installments *inst in [methodResponse installments]){
                             NSLog(@"%@", [inst numPayments]);
                             NSLog(@"%@", [inst installmentAmount]);
                         }

                         NSLog(@"%@", [methodResponse posDateTime]);
                     }
                 }];;