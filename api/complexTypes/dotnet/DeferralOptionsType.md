RootElement data = new RootElement();


ComplexElement DeferralOptions = new ComplexElement();
DeferralOptions.Add("FirstPaymentDeferral", "1");
DeferralOptions.Add("Amount", "10000");

data.Add("DeferralOptions", DeferralOptions);
