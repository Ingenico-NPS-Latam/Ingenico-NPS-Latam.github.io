import com.github.ingeniconpslatam.nps.Card;
import com.github.ingeniconpslatam.nps.InstallmentOption;
import com.github.ingeniconpslatam.nps.Nps;
import com.github.ingeniconpslatam.nps.PaymentMethod;
import com.github.ingeniconpslatam.nps.PaymentMethodToken;


Nps nps = new Nps(Nps.SANDBOX, "__YOUR_NPS_CLIENT_SESSION__", "__YOUR_NPS_MERCHANT_ID__");

String paymentMethodTokenId = "HGIYeXKJpQyBvO3pHuZTN9JZiVPnzQaQ";

nps.retrievePaymentMethodToken(paymentMethodTokenId, new Nps.ResponseHandler() {
    @Override
        public void onSuccess(PaymentMethodToken paymentMethodToken) {
            Log.d("Nps", "token success = " + paymentMethodToken.getId());
        }

        @Override
        public void onError(Exception error) {
            Log.d("Nps", "token error");
        }
    });
}
