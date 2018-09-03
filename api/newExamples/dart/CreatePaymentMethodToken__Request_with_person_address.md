import 'dart:async';

import 'package:nps_sdk/nps_sdk.dart';

main(List<String> arguments) async {
  Nps nps = new Nps(sandbox);

  Map createPaymentMethodTokenParams = {
    "psp_Version": "2.2",
    "psp_MerchantId": "sdk_test",
    "psp_CardInputDetails": {
      "Number": "4507990000000010",
      "ExpirationDate": "2501",
      "SecurityCode": "123",
      "HolderName": "JOHN DOE"
    },
    "Person": {
        "FirstName": "John",
        "LastName": "Doe",
        "MiddleName": "Michael",
        "PhoneNumber1": "+1 011 11111111",
        "PhoneNumber2": "+1 011 22222222",
        "DateOfBirth": "1979-01-12",
        "Gender": "M",
        "Nationality": "ARG",
        "IDNumber": "54111111",
        "IDType": "200"
    },
    "Address": {
        "Street": "Av. Collins",
        "HouseNumber": "4702",
        "AdditionalInfo": "2 A",
        "City": "Buenos Aires",
        "StateProvince": "CABA",
        "Country": "ARG",
        "ZipCode": "1425"
    },
    "psp_ClientSession": "YOUR_CLIENT_SESSION"
  };

  Future response = nps.createPaymentMethodToken(nps, createPaymentMethodTokenParams);
  response
    .then((resp) {
      //Handle your response here
    })
    .catchError((error) {
      //Handle your error here
    });
}