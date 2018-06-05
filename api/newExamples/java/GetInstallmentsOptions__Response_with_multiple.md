import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.getInstallmentsOptions(data);

response.getValue("psp_ResponseCod");
response.getValue("psp_ResponseMsg");
response.getValue("psp_MerchantId");
response.getValue("psp_Amount");
response.getValue("psp_Product");
response.getValue("psp_Currency");
response.getValue("psp_Country");
response.getValue("psp_NumPayments");

List<ComplexElementArrayItem> pspInstallmentsOptions = response.getComplexElementArray('psp_InstallmentsOptions');

ComplexElementArrayItem pspInstallmentsOptions1 = pspInstallmentsOptions.getValue(1);
pspInstallmentsOptions1.getValue("NumPayments");
pspInstallmentsOptions1.getValue("InstallmentAmount");


response.getValue("psp_PosDateTime");
