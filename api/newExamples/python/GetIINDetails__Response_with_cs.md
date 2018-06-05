response = sdk.get_iin_details(params)

response.get('psp_ResponseCod')
response.get('psp_ResponseMsg')
response.get('psp_MerchantId')
response.get('psp_Product')
response.get('psp_PosDateTime')
