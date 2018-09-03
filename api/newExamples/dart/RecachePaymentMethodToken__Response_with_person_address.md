Future response = nps.recachePaymentMethodToken(nps, recachePaymentMethodTokenParams);
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
      
      print(resp["psp_Person"]["FirstName"]);
      print(resp["psp_Person"]["LastName"]);
      print(resp["psp_Person"]["MiddleName"]);
      print(resp["psp_Person"]["PhoneNumber1"]);
      print(resp["psp_Person"]["PhoneNumber2"]);
      print(resp["psp_Person"]["Gender"]);
      print(resp["psp_Person"]["DateOfBirth"]);
      print(resp["psp_Person"]["Nationality"]);
      print(resp["psp_Person"]["IDNumber"]);
      print(resp["psp_Person"]["IDType"]);
      
      print(resp["psp_Address"]["Street"]);
      print(resp["psp_Address"]["HouseNumber"]);
      print(resp["psp_Address"]["AdditionalInfo"]);
      print(resp["psp_Address"]["City"]);
      print(resp["psp_Address"]["StateProvince"]);
      print(resp["psp_Address"]["Country"]);
      print(resp["psp_Address"]["ZipCode"]);
          
      print(resp["psp_AlreadyUsed"]);
      print(resp["psp_CreatedAt"]);
      print(resp["psp_UpdatedAt"]);
    })
    .catchError((error) {
      //Handle your error here
    });