pspAmountAdditionalDetails := resp.Psp_AmountAdditionalDetails
fmt.Printf(pspAmountAdditionalDetails.Tip)
fmt.Printf(pspAmountAdditionalDetails.Discount)

taxes := psp_AmountAdditionalDetails.Taxes

taxes1 := taxes.Items[1];
fmt.Printf(taxes1.TypeId)
fmt.Printf(taxes1.TypeDescription)
fmt.Printf(taxes1.Amount)

rate := taxes1.Rate


baseAmount := taxes1.BaseAmount


appliedAmount := taxes1.AppliedAmount


remarks := taxes1.Remarks

taxes2 := taxes.Items[2];
fmt.Printf(taxes2.TypeId)
fmt.Printf(taxes2.TypeDescription)
fmt.Printf(taxes2.Amount)
fmt.Printf(taxes2.Rate)
fmt.Printf(taxes2.BaseAmount)

appliedAmount := taxes2.AppliedAmount


remarks := taxes2.Remarks