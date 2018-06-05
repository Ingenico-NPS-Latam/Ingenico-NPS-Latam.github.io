
response = nps.create_client_session(createclientsession)

print(response.psp_ResponseCod)
print(response.psp_ResponseMsg)
print(response.psp_MerchantId)
print(response.psp_ClientSession)
print(response.psp_PosDateTime)
print(response.psp_CreatedAt)
