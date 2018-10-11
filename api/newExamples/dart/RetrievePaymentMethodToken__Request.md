import 'dart:async';

import 'package:nps_sdk/nps_sdk.dart';

main(List<String> arguments) async {
  Nps nps = new Nps(sandbox);

  Map retrievePaymentMethodTokenParams = {
        "psp_Version": "2.2",
        "psp_MerchantId": "sdk_test",
        "psp_PaymentMethodToken": "YOUR_PAYMENT_METHOD_TOKEN",
        "psp_ClientSession": "YOUR_CLIENT_SESSION",
        "psp_PosDateTime": "2008-01-12 13:05:00"
    };

  Future response = nps.retrievePaymentMethodToken(nps, retrievePaymentMethodTokenParams);
  response
    .then((resp) {
      //Handle your response here
    })
    .catchError((error) {
      //Handle your error here
    });
}