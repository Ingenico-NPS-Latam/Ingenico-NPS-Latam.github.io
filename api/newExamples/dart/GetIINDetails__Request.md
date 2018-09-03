import 'dart:async';

import 'package:nps_sdk/nps_sdk.dart';

main(List<String> arguments) async {
  Nps nps = new Nps(sandbox);

  Map getINNDetailsParams = {
        "psp_Version" : "2.2",
        "psp_MerchantId" : "sdk_test",
        "psp_IIN" : "424242",
        "psp_PosDateTime" : "2019-12-01 12:00:00",
        "psp_ClientSession": "YOUR_CLIENT_SESSION"
    };

  Future response = nps.getINNDetails(nps, getINNDetailsParams);
  response
    .then((resp) {
      //Handle your response here
    })
    .catchError((error) {
      //Handle your error here
    });
}