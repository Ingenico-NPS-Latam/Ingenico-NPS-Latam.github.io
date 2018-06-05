resp, err := service.amountDetailsResponseType.md(amountDetailsResponseType.md)


amountDetailResponse := resp.AmountDetailResponse
fmt.Printf(amountDetailResponse.Tip)
fmt.Printf(amountDetailResponse.Discount)

taxes := AmountDetailResponse.Taxes

taxes1 := taxes.Items[1];
fmt.Printf(taxes1.TypeId)
fmt.Printf(taxes1.Amount)
fmt.Printf(taxes1.Rate)
fmt.Printf(taxes1.BaseAmount)


taxes2 := taxes.Items[2];
fmt.Printf(taxes2.TypeId)
fmt.Printf(taxes2.Amount)
fmt.Printf(taxes2.Rate)
fmt.Printf(taxes2.BaseAmount)



