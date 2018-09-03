import com.github.ingeniconpslatam.nps.Card;
import com.github.ingeniconpslatam.nps.InstallmentOption;
import com.github.ingeniconpslatam.nps.Nps;
import com.github.ingeniconpslatam.nps.PaymentMethod;
import com.github.ingeniconpslatam.nps.PaymentMethodToken;


Nps nps = new Nps(Nps.SANDBOX, "__YOUR_NPS_CLIENT_SESSION__", "__YOUR_NPS_MERCHANT_ID__");

PaymentMethod paymentMethod = new PaymentMethod();
paymentMethod.setId('51e0kuKSwkG3GlaGq2fQaNdBsfOY0EHY');
paymentMethod.setCardSecurityCode("123");

nps.recachePaymentMethodToken(paymentMethod, null, new Nps.ResponseHandler() {
        @Override
        public void onSuccess(PaymentMethodToken paymentMethodToken) {
            Log.d("Nps", "token success = " + paymentMethodToken.getId());
        }

        @Override
        public void onError(Exception error) {
            Log.d("Nps", "token error");
        }
    });