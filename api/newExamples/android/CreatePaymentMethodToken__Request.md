import com.github.ingeniconpslatam.nps.Card;
import com.github.ingeniconpslatam.nps.InstallmentOption;
import com.github.ingeniconpslatam.nps.Nps;
import com.github.ingeniconpslatam.nps.PaymentMethod;
import com.github.ingeniconpslatam.nps.PaymentMethodToken;


Nps nps = new Nps(Nps.SANDBOX, "__YOUR_NPS_CLIENT_SESSION__", "__YOUR_NPS_MERCHANT_ID__");

Card card = new Card()
        .setHolderName("John Smith")
        .setNumber("4507990000000010")
        .setExpirationDate("1912")
        .setSecurityCode("123")
        .setNumPayments("1");

Billing billing = new Billing();

billing.getPerson()
          .setFirstName("John")
          .setLastName("Smith")
          .setDateOfBirth("1987-01-01")
          .setGender("M")
          .setNationality("ARG")
          .setIdType(Billing.IDTYPE_AR_DNI)
          .setIdNumber("32123123")
          .setPhoneNumber1("4123-1234")
          .setPhoneNumber2("4123-5678");

billing.getAddress()
          .setAdditionalInfo("adding additional info")
          .setCity("Capital Federal")
          .setStateProvince("Capital Federal")
          .setCountry("ARG")
          .setZipCode("1414")
          .setStreet("Calle Falsa")
          .setHouseNumber("123");

nps.createPaymentMethodToken(card, billing,
    new Nps.ResponseHandler() {
        @Override
        public void onSuccess(PaymentMethodToken paymentMethodToken) {
            Log.d("Nps", "token success = " + paymentMethodToken.getId());
        }

        @Override
        public void onError(Exception error) {
            Log.d("Nps", "token error");
        }
    });