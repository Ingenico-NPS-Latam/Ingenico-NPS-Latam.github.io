import 'dart:async';

import 'package:nps_sdk/nps_sdk.dart';

main(List<String> arguments) async {
  Nps nps = new Nps(sandbox);

  Map getInstallmentsOptionsParams = {
        "psp_Version": "2.2",
        "psp_MerchantId": "sdk_test",
        "psp_Amount": "100",
        "psp_Product": "14",
        "psp_Currency": "152",
        "psp_Country": "CHL",
        "psp_NumPayments": "1",
        "psp_PaymentMethodToken": "YOUR_PAYMENT_METHOD_TOKEN",
        "psp_ClientSession": "YOUR_CLIENT_SESSION",
        "psp_PosDateTime": "2017-04-04 13:35:20"
    };
    
  Future response = nps.getInstallmentsOptions(nps, getInstallmentsOptionsParams);
  response
    .then((resp) {
      //Handle your response here
    })
    .catchError((error) {
      //Handle your error here
    });
}