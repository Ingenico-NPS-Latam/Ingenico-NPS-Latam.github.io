nps.recachePaymentMethodToken(paymentMethod, billing, new Nps.ResponseHandler() {
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

            Billing billing = paymentMethodToken.getBilling();

            Person person = billing.getPerson();
            Log.d("Nps", person.getFirstName();
            Log.d("Nps", person.getLastName();
            Log.d("Nps", person.getMiddleName();
            Log.d("Nps", person.getPhoneNumber1();
            Log.d("Nps", person.getPhoneNumber2();
            Log.d("Nps", person.getGender();
            Log.d("Nps", person.getDateOfBirth();
            Log.d("Nps", person.getNationality();
            Log.d("Nps", person.getIdNumber();
            Log.d("Nps", person.getIdType();

            Person address = billing.getAddress();
            Log.d("Nps", address.getStreet();
            Log.d("Nps", address.getHouseNumber();
            Log.d("Nps", address.getAdditionalInfo();
            Log.d("Nps", address.getCity();
            Log.d("Nps", address.getStateProvince();
            Log.d("Nps", address.getCountry();
            Log.d("Nps", address.getZipCode();

            Log.d("Nps", paymentMethodToken.createdAt();
            Log.d("Nps", paymentMethodToken.alreadyUsed();
            Log.d("Nps", paymentMethodToken.updateAt();
        }

        @Override
        public void onError(Exception error) {
            Log.d("Nps", "token error");
        }
    });