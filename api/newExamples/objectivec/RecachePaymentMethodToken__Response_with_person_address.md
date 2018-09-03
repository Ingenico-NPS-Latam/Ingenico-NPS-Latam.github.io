[nps recachePaymentMethodToken:@"kWRZGcAxy5D7MoB6BDACugHYrlFzP9Eg"
              cardSecurityCode:@"123"
                billingDetails:billingDetailss
                methodResponse:^(NpsRecachePaymentMethodTokenResponse *methodResponse, NSError *error) {
                    if (!error){
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

                        NpsPerson *person = [methodResponse person]);
                        NSLog(@"%@", [person firstName]);
                        NSLog(@"%@", [person lastName]);
                        NSLog(@"%@", [person middleName]);
                        NSLog(@"%@", [person phoneNumber1]);
                        NSLog(@"%@", [person phoneNumber2]);
                        NSLog(@"%@", [person gender]);
                        NSLog(@"%@", [person dateOfBirth]);
                        NSLog(@"%@", [person nationality]);
                        NSLog(@"%@", [person idNumber]);
                        NSLog(@"%@", [person idType]);

                        NpsPerson *address = [methodResponse address]);
                        NSLog(@"%@", [address street]);
                        NSLog(@"%@", [address houseNumber]);
                        NSLog(@"%@", [address additionalInfo]);
                        NSLog(@"%@", [address city]);
                        NSLog(@"%@", [address stateProvince]);
                        NSLog(@"%@", [address country]);
                        NSLog(@"%@", [address zipCode]);

                        NSLog(@"%@", [methodResponse alreadyUsed]);
                        NSLog(@"%@", [methodResponse createdAt]);
                        NSLog(@"%@", [methodResponse updateAt]);
                    }
}];