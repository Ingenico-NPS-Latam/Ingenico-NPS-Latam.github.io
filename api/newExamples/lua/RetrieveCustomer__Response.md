
response = nps.retrieve_customer(retrievecustomer)

print(response.psp_ResponseCod)
print(response.psp_ResponseMsg)
print(response.psp_MerchantId)
print(response.psp_CustomerId)
print(response.psp_EmailAddress)
print(response.psp_AlternativeEmailAddress)
print(response.psp_AccountID)
print(response.psp_AccountCreatedAt)
print(response.psp_PosDateTime)
