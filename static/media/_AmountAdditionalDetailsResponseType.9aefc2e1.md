pspAmountAdditionalDetails = response[:psp_amountadditional_details];
pspAmountAdditionalDetails[:tip];
pspAmountAdditionalDetails[:discount];

taxes0 = pspAmountAdditionalDetails[:taxes][0];

taxes0[:type_id];
taxes0[:type_description];
taxes0[:amount];

rate = taxes0[:rate];


baseAmount = taxes0[:base_amount];


appliedAmount = taxes0[:appliedamount];


remarks = taxes0[:remarks];


taxes1 = pspAmountAdditionalDetails[:taxes][1];

taxes1[:type_id];
taxes1[:type_description];
taxes1[:amount];
taxes1[:rate];
taxes1[:base_amount];

appliedAmount = taxes1[:appliedamount];


remarks = taxes1[:remarks];