import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement deferralOptions = response.getComplexElement("DeferralOptions");


ComplexElement deferralOptions = deferralOptions.getComplexElement("DeferralOptions");
deferralOptions.getValue("FirstPaymentDeferral");
deferralOptions.getValue("Amount");

