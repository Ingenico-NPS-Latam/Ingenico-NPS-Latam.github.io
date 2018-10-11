import 'dart:async';

import 'package:nps_sdk/nps_sdk.dart';

main(List<String> arguments) async {
  Nps nps = new Nps(sandbox);

  Map createPaymentMethodTokenParams = {
    "psp_Version": "2.2",
    "psp_MerchantId": "sdk_test",
    "psp_WalletInputDetails": {
        "WalletTypeId": "2",
        "WalletKey": "d084703513e87cd1540a114cd7317e6642eca04e",
        "MerchOrderId": "1efed583-1824-436a-869f-286ebdb22ae9"
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