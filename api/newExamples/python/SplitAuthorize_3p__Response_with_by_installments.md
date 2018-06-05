response = sdk.split_authorize_3p(params)

response.get('psp_ResponseCod')
response.get('psp_ResponseMsg')
response.get('psp_TransactionId')
response.get('psp_Session3p')
response.get('psp_FrontPSP_URL')
response.get('psp_MerchantId')
response.get('psp_MerchTxRef')
response.get('psp_MerchOrderId')
response.get('psp_Amount')
response.get('psp_Currency')
response.get('psp_Country')
response.get('psp_Product')
response.get('psp_PosDateTime')

pspTransactions0 = response.get('psp_Transactions')[0]

pspTransactions0.get('psp_MerchantId')
pspTransactions0.get('psp_TransactionId')
pspTransactions0.get('psp_MerchTxRef')
pspTransactions0.get('psp_Product')
pspTransactions0.get('psp_Amount')
pspTransactions0.get('psp_NumPayments')
pspTransactions0.get('psp_CreatedAt')

pspTransactions1 = response.get('psp_Transactions')[1]

pspTransactions1.get('psp_MerchantId')
pspTransactions1.get('psp_TransactionId')
pspTransactions1.get('psp_MerchTxRef')
pspTransactions1.get('psp_Product')
pspTransactions1.get('psp_Amount')
pspTransactions1.get('psp_NumPayments')
pspTransactions1.get('psp_CreatedAt')


