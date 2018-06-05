response = sdk.query_card_number(params)

response.get('psp_ResponseCod')
response.get('psp_ResponseMsg')
response.get('psp_MerchantId')
response.get('psp_QueryCriteria')
response.get('psp_QueryCriteriaId')
response.get('psp_PosDateTime')
response.get('psp_CardNumber')
