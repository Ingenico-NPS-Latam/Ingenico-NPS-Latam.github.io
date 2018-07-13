RootElement data = new RootElement();


ComplexElement DeferralOptions = new ComplexElement();
DeferralOptions.add("FirstPaymentDeferral", "1");
DeferralOptions.add("Amount", "10000");

data.add("DeferralOptions", DeferralOptions);
