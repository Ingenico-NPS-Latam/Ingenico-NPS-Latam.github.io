response = sdk.fraud_screening(params)

response.get('psp_ResponseCod')
response.get('psp_ResponseMsg')

pspResult = response.get('psp_Result')
pspResult.get('ResultCode')
pspResult.get('ResultDescription')
response.get('psp_OrderId')
response.get('psp_MerchantId')
response.get('psp_MerchTxRef')
response.get('psp_MerchOrderId')
response.get('psp_Amount')
response.get('psp_NumPayments')
response.get('psp_Currency')
response.get('psp_Country')
response.get('psp_Product')
response.get('psp_CardNumber')
response.get('psp_CardExpDate')
response.get('psp_PosDateTime')
