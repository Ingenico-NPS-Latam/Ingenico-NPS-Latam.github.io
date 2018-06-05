response = sdk.create_client_session(params)

response.get('psp_ResponseCod')
response.get('psp_ResponseMsg')
response.get('psp_MerchantId')
response.get('psp_ClientSession')
response.get('psp_PosDateTime')
response.get('psp_CreatedAt')
