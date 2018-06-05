[nps getIIDetails:@"424242"
   postDateTime:@"2016-12-01 12:00:00"
 methodResponse:^(NpsGetIINDetailsResponse *methodResponse, NSError *error) {
    if(!error){
        NSLog(@"%@", [methodResponse responseCod]);
        NSLog(@"%@", [methodResponse responseMsg]);
        NSLog(@"%@", [methodResponse merchandId]);
        NSLog(@"%@", [methodResponse product]);
        NSLog(@"%@", [methodResponse posDateTime]);
    }
}];