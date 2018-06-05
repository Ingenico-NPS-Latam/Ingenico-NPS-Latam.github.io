local pspAmountAdditionalDetails = resp.psp_AmountAdditionalDetails
print(pspAmountAdditionalDetails.Tip)
print(pspAmountAdditionalDetails.Discount)

local taxes = psp_AmountAdditionalDetails.Taxes

localtaxes1 := taxes[1]
print(taxes1.TypeId)
print(taxes1.TypeDescription)
print(taxes1.Amount)

local rate = taxes1.Rate


local baseAmount = taxes1.BaseAmount


local appliedAmount = taxes1.AppliedAmount


local remarks = taxes1.Remarks



localtaxes2 := taxes[2]
print(taxes2.TypeId)
print(taxes2.TypeDescription)
print(taxes2.Amount)
print(taxes2.Rate)
print(taxes2.BaseAmount)

local appliedAmount = taxes2.AppliedAmount


local remarks = taxes2.Remarks