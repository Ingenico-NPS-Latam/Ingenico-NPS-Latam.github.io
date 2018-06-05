[nps createPaymentMethodToken:card
               billingDetails:billing
              methodResponse:^(NpsCreatePaymentMethodTokenResponse* methodResponse, NSError *error) {
                if(!error){
                    NSLog(@"%@", [methodResponse responseCod]);
                    NSLog(@"%@", [methodResponse responseMsg]);
                    NSLog(@"%@", [methodResponse merchandId]);
                    NSLog(@"%@", [methodResponse paymentMethodToken]);
                    NSLog(@"%@", [methodResponse product]);

                    NpsCardDetails *cardDetails = [methodResponse cardDetails]);
                    NSLog(@"%@", [cardDetails expirationDate]);
                    NSLog(@"%@", [cardDetails expirationYear]);
                    NSLog(@"%@", [cardDetails expirationMonth]);
                    NSLog(@"%@", [cardDetails holderName]);
                    NSLog(@"%@", [cardDetails IIN]);
                    NSLog(@"%@", [cardDetails last4]);
                    NSLog(@"%@", [cardDetails numberLength]);
                    NSLog(@"%@", [cardDetails maskedNumber]);
                    NSLog(@"%@", [cardDetails maskedNumberAlternative]);

                    NSLog(@"%@", [methodResponse createdAt]);
                    NSLog(@"%@", [methodResponse alreadyUsed]);
                    NSLog(@"%@", [methodResponse updateAt]);
                }
}];