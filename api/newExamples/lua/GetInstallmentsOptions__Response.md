
response = nps.get_installments_options(getinstallmentsoptions)

print(response.psp_ResponseCod)
print(response.psp_ResponseMsg)
print(response.psp_MerchantId)
print(response.psp_Amount)
print(response.psp_Product)
print(response.psp_Currency)
print(response.psp_Country)
print(response.psp_NumPayments)

local pspInstallmentsOptions = response.Psp_InstallmentsOptions

localpspInstallmentsOptions1 := pspInstallmentsOptions[1]
print(pspInstallmentsOptions1.NumPayments)
print(pspInstallmentsOptions1.InstallmentAmount)


print(response.psp_PosDateTime)
