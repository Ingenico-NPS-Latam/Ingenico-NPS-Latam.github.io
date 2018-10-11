import com.github.ingeniconpslatam.nps.Card;
import com.github.ingeniconpslatam.nps.InstallmentOption;
import com.github.ingeniconpslatam.nps.Nps;
import com.github.ingeniconpslatam.nps.PaymentMethod;
import com.github.ingeniconpslatam.nps.PaymentMethodToken;


Nps nps = new Nps(Nps.SANDBOX, "__YOUR_NPS_CLIENT_SESSION__", "__YOUR_NPS_MERCHANT_ID__");

Wallet wallet = new Wallet()
        .setTypeId("2")
        .setKey("d084703513e87cd1540a114cd7317e6642eca04e")
        .setMerchOrderId("1efed583-1824-436a-869f-286ebdb22ae9");

nps.createPaymentMethodToken(null, null, wallet,
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