using System;
using NpsSDK;

RootElement response = npsSdk.GetInstallmentsOptions(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_MerchantId");
response.GetValue("psp_Amount");
response.GetValue("psp_Product");
response.GetValue("psp_Currency");
response.GetValue("psp_Country");
response.GetValue("psp_NumPayments");

ComplexElementArray pspInstallmentsOptions = response.GetComplexElementArray("psp_InstallmentsOptions");

ComplexElementArrayItem pspInstallmentsOptions1 = pspInstallmentsOptions[1];
pspInstallmentsOptions1.GetValue("NumPayments");
pspInstallmentsOptions1.GetValue("InstallmentAmount");


response.GetValue("psp_PosDateTime");
