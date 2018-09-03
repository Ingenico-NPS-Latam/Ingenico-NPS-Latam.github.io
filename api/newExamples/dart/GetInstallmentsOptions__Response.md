Future response = nps.getInstallmentsOptions(nps, getInstallmentsOptionsParams);
  response
    .then((resp) {
      print(resp["psp_ResponseCod"]);
      print(resp["psp_ResponseMsg"]);
      print(resp["psp_MerchantId"]);
      print(resp["psp_Amount"]);
      print(resp["psp_Product"]);
      print(resp["psp_Currency"]);
      print(resp["psp_Country"]);
      print(resp["psp_NumPayments"]);
      
      print(resp["psp_InstallmentsOptions"]["NumPayments"]);
      print(resp["psp_InstallmentsOptions"]["InstallmentAmount"]);
      
      print(resp["psp_PosDateTime"]);
    })
    .catchError((error) {
      //Handle your error here
});