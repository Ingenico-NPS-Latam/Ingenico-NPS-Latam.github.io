import com.github.ingeniconpslatam.nps.Card;
import com.github.ingeniconpslatam.nps.InstallmentOption;
import com.github.ingeniconpslatam.nps.Nps;
import com.github.ingeniconpslatam.nps.PaymentMethod;
import com.github.ingeniconpslatam.nps.PaymentMethodToken;


Nps nps = new Nps(Nps.SANDBOX, "__YOUR_NPS_CLIENT_SESSION__", "__YOUR_NPS_MERCHANT_ID__");
nps.setAmount('120050');
nps.setCountry('CHL');
nps.setCurrency('152');

ArrayList<InstallmentOption> installments = nps.getInstallmentsOptions('8T3BOsXaLMxVsvtHiSuWKL1DEOUUDq3N', '14', '3');