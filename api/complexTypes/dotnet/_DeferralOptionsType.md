using System;
using NpsSDK;

ComplexElement DeferralOptions = response.GetComplexElement("DeferralOptions");


ComplexElement deferralOptions = DeferralOptions.GetComplexElement("DeferralOptions");
deferralOptions.GetValue("FirstPaymentDeferral");
deferralOptions.GetValue("Amount");

