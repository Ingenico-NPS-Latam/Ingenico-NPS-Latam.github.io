
response = nps.get_iin_details(getiindetails)

print(response.psp_ResponseCod)
print(response.psp_ResponseMsg)
print(response.psp_MerchantId)
print(response.psp_Product)
print(response.psp_PosDateTime)
