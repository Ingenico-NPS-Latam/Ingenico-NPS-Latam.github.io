resp = nps.amountDetailsResponseType.md(amountDetailsResponseType.md)


local amountDetailResponse = resp.AmountDetailResponse
print(amountDetailResponse.Tip)
print(amountDetailResponse.Discount)

local taxes = AmountDetailResponse.Taxes

localtaxes1 := taxes[1]
print(taxes1.TypeId)
print(taxes1.Amount)
print(taxes1.Rate)
print(taxes1.BaseAmount)


localtaxes2 := taxes[2]
print(taxes2.TypeId)
print(taxes2.Amount)
print(taxes2.Rate)
print(taxes2.BaseAmount)



