{
    pspAmountAdditionalDetails = {}
    pspAmountAdditionalDetails.Tip = "20"
    pspAmountAdditionalDetails.Discount = "1"
    
    Taxes = {}
    
    Taxes1 = {}
    Taxes1.TypeId = "600"
    Taxes1.Amount = "100"
    Taxes1.Rate = "21"
    Taxes1.BaseAmount = "10"
    
    Taxes[#Taxes+1] = Taxes1
    
    Taxes2 = {}
    Taxes2.TypeId = "601"
    Taxes2.Amount = "100"
    Taxes2.Rate = "21"
    Taxes2.BaseAmount = "10"
    
    Taxes[#Taxes+1] = Taxes2
    
    pspAmountAdditionalDetails.Taxes = Taxes
    
    payonline2p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails
}