[nps getIIDetails:@"424242"
 methodResponse:^(NpsGetIINDetailsResponse *methodResponse, NSError *error) {
    if(!error){
        NSLog(@"%@", [methodResponse responseCod]);
        NSLog(@"%@", [methodResponse responseMsg]);
        NSLog(@"%@", [methodResponse merchandId]);
        NSLog(@"%@", [methodResponse product]);
        NSLog(@"%@", [methodResponse posDateTime]);
    }
}];