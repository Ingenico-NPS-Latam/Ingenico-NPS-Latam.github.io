
resp = nps.notify_fraud_screening_review(notifyfraudscreeningreview)

print(resp.psp_ResponseCod)
print(resp.psp_ResponseMsg)
print(resp.psp_ResponseExtended)
print(resp.psp_MerchantId)
print(resp.psp_PosDateTime)
