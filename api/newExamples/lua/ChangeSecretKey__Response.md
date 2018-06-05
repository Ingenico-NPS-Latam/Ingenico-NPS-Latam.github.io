
response = nps.change_secret_key(changesecretkey)

print(response.psp_ResponseCod)
print(response.psp_ResponseMsg)
print(response.psp_MerchantId)
print(response.psp_PosDateTime)
