ComplexElement deferralOptions = response.getComplexElement("DeferralOptions");


local deferralOptions = deferralOptions.DeferralOptions
print(deferralOptions.FirstPaymentDeferral)
print(deferralOptions.Amount)

