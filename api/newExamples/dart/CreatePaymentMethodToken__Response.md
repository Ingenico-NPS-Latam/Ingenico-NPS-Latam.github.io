Future response = nps.createPaymentMethodToken(nps, createPaymentMethodTokenParams);
  response
    .then((resp) {
      print(resp["psp_ResponseCod"]);
      print(resp["psp_ResponseMsg"]);
      print(resp["psp_MerchantId"]);
      print(resp["psp_PaymentMethodToken"]);
      print(resp["psp_Product"]);

      print(resp["psp_CardOutputDetails"]["ExpirationDate"]);
      print(resp["psp_CardOutputDetails"]["ExpirationYear"]);
      print(resp["psp_CardOutputDetails"]["ExpirationMonth"]);
      print(resp["psp_CardOutputDetails"]["HolderName"]);
      print(resp["psp_CardOutputDetails"]["IIN"]);
      print(resp["psp_CardOutputDetails"]["Last4"]);
      print(resp["psp_CardOutputDetails"]["NumberLength"]);
      print(resp["psp_CardOutputDetails"]["MaskedNumber"]);
      print(resp["psp_CardOutputDetails"]["MaskedNumberAlternative"]);      

      print(resp["psp_AlreadyUsed"]);
      print(resp["psp_CreatedAt"]);
      print(resp["psp_UpdatedAt"]);
    })
    .catchError((error) {
      //Handle your error here
});