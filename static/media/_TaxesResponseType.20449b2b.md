import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.taxesResponseType.md(data);


ComplexElement taxesResponse = response.getComplexElement("TaxesResponse");
taxesResponse.getValue("TypeId");
taxesResponse.getValue("TypeDescription");
taxesResponse.getValue("Amount");
taxesResponse.getValue("Rate");
taxesResponse.getValue("BaseAmount");
taxesResponse.getValue("AppliedAmount");
taxesResponse.getValue("Remarks");

