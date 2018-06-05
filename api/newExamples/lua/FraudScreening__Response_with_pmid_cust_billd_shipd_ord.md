
response = nps.fraud_screening(fraudscreening)

print(response.psp_ResponseCod)
print(response.psp_ResponseMsg)

local pspResult = response.psp_Result
print(pspResult.ResultCode)
print(pspResult.ResultDescription)

print(response.psp_OrderId)
print(response.psp_MerchantId)
print(response.psp_MerchTxRef)
print(response.psp_MerchOrderId)
print(response.psp_Amount)
print(response.psp_NumPayments)
print(response.psp_Currency)
print(response.psp_Country)
print(response.psp_Product)
print(response.psp_CardExpDate)
print(response.psp_PosDateTime)
