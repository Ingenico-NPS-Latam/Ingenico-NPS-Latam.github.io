Future response = nps.getINNDetails(nps, getINNDetailsParams);
  response
    .then((resp) {
      print(resp["psp_ResponseCod"]);
      print(resp["psp_ResponseMsg"]);
      print(resp["psp_MerchantId"]);
      print(resp["psp_Product"]);
      print(resp["psp_PosDateTime"]);
    })
    .catchError((error) {
      //Handle your error here
});