
resp = nps.query_card_details(querycarddetails)

print(resp.psp_ResponseCod)
print(resp.psp_ResponseMsg)
print(resp.psp_MerchantId)
print(resp.psp_QueryCriteria)
print(resp.psp_QueryCriteriaId)
print(resp.psp_PosDateTime)

local pspCardOutputDetails = resp.psp_CardOutputDetails
print(pspCardOutputDetails.Number)
print(pspCardOutputDetails.ExpirationDate)
print(pspCardOutputDetails.ExpirationYear)
print(pspCardOutputDetails.ExpirationMonth)
print(pspCardOutputDetails.HolderName)
print(pspCardOutputDetails.IIN)
print(pspCardOutputDetails.Last4)
print(pspCardOutputDetails.NumberLength)
print(pspCardOutputDetails.MaskedNumber)
print(pspCardOutputDetails.MaskedNumberAlternative)

