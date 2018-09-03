nps.createPaymentMethodToken(card, billing,
    new Nps.ResponseHandler() {
        @Override
        public void onSuccess(PaymentMethodToken paymentMethodToken) {
            Log.d("Nps", paymentMethodToken.getResponseCod();
            Log.d("Nps", paymentMethodToken.getResponseMsg();
            Log.d("Nps", paymentMethodToken.getMerchantId();
            Log.d("Nps", paymentMethodToken.getId();
            Log.d("Nps", paymentMethodToken.getProduct();

            CardOutputDetails cardDetails = paymentMethodToken.getCardOutputDetails();
            Log.d("Nps", cardDetails.getExpirationDate();
            Log.d("Nps", cardDetails.getExpirationYear();
            Log.d("Nps", cardDetails.getExpirationMonth();
            Log.d("Nps", cardDetails.getHolderName();
            Log.d("Nps", cardDetails.getIIN();
            Log.d("Nps", cardDetails.getLast4();
            Log.d("Nps", cardDetails.getNumberLength();
            Log.d("Nps", cardDetails.getMaskedNumber();
            Log.d("Nps", cardDetails.getMaskedNumberAlternative();

            Log.d("Nps", paymentMethodToken.createdAt();
            Log.d("Nps", paymentMethodToken.alreadyUsed();
            Log.d("Nps", paymentMethodToken.updateAt();
        }

        @Override
        public void onError(Exception error) {
            Log.d("Nps", "token error");
        }
    });



