response = sdk.get_installments_options(params)

response.get('psp_ResponseCod')
response.get('psp_ResponseMsg')
response.get('psp_MerchantId')
response.get('psp_Amount')
response.get('psp_Product')
response.get('psp_Currency')
response.get('psp_Country')
response.get('psp_NumPayments')

pspInstallmentsOptions0 = response.get('psp_InstallmentsOptions')[0]

pspInstallmentsOptions0.get('NumPayments')
pspInstallmentsOptions0.get('InstallmentAmount')


response.get('psp_PosDateTime')
