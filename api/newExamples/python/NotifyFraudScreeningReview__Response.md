response = sdk.notify_fraud_screening_review(params)

response.get('psp_ResponseCod')
response.get('psp_ResponseMsg')
response.get('psp_ResponseExtended')
response.get('psp_MerchantId')
response.get('psp_PosDateTime')
