
response = nps.query_card_number(querycardnumber)

print(response.psp_ResponseCod)
print(response.psp_ResponseMsg)
print(response.psp_MerchantId)
print(response.psp_QueryCriteria)
print(response.psp_QueryCriteriaId)
print(response.psp_PosDateTime)
print(response.psp_CardNumber)
