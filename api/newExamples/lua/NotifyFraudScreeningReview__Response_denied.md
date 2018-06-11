
response = nps.notify_fraud_screening_review(notifyfraudscreeningreview)

print(response.psp_ResponseCod)
print(response.psp_ResponseMsg)
print(response.psp_MerchantId)
print(response.psp_PosDateTime)
