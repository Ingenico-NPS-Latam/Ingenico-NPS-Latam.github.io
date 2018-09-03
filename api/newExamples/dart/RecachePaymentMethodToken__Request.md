import 'dart:async';

import 'package:nps_sdk/nps_sdk.dart';

main(List<String> arguments) async {
  Nps nps = new Nps(sandbox);

  Map recachePaymentMethodTokenParams = {
        "psp_Version": "2.2",
        "psp_MerchantId": "sdk_test",
        "psp_CardSecurityCode": "123",
        "psp_PaymentMethodId": "YOUR_PAYMENT_METHOD",
        "psp_ClientSession": "YOUR_CLIENT_SESSION"
    };
    
  Future response = nps.recachePaymentMethodToken(nps, recachePaymentMethodTokenParams);
  response
    .then((resp) {
      //Handle your response here
    })
    .catchError((error) {
      //Handle your error here
    });
}