ComplexElement deferralOptions = response.getComplexElement("DeferralOptions");


deferralOptions := deferralOptions.DeferralOptions
fmt.Printf(deferralOptions.FirstPaymentDeferral)
fmt.Printf(deferralOptions.Amount)

