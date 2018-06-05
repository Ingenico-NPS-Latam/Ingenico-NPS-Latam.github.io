
response = nps.split_authorize_3p(splitauthorize3p)

print(response.psp_ResponseCod)
print(response.psp_ResponseMsg)
print(response.psp_TransactionId)
print(response.psp_Session3p)
print(response.psp_FrontPSP_URL)
print(response.psp_MerchantId)
print(response.psp_MerchTxRef)
print(response.psp_MerchOrderId)
print(response.psp_Amount)
print(response.psp_Currency)
print(response.psp_Country)
print(response.psp_Product)
print(response.psp_PosDateTime)

local pspTransactions = response.Psp_Transactions

localpspTransactions1 := pspTransactions[1]
print(pspTransactions1.psp_MerchantId)
print(pspTransactions1.psp_TransactionId)
print(pspTransactions1.psp_MerchTxRef)
print(pspTransactions1.psp_Product)
print(pspTransactions1.psp_Amount)
print(pspTransactions1.psp_NumPayments)
print(pspTransactions1.psp_CreatedAt)


localpspTransactions2 := pspTransactions[2]
print(pspTransactions2.psp_MerchantId)
print(pspTransactions2.psp_TransactionId)
print(pspTransactions2.psp_MerchTxRef)
print(pspTransactions2.psp_Product)
print(pspTransactions2.psp_Amount)
print(pspTransactions2.psp_NumPayments)
print(pspTransactions2.psp_CreatedAt)


