using System;
using NpsSDK;

RootElement response = npsSdk.TaxesResponseType.md(data);


ComplexElement taxesResponse = response.GetComplexElement("TaxesResponse");
taxesResponse.GetValue("TypeId");
taxesResponse.GetValue("TypeDescription");
taxesResponse.GetValue("Amount");
taxesResponse.GetValue("Rate");
taxesResponse.GetValue("BaseAmount");
taxesResponse.GetValue("AppliedAmount");
taxesResponse.GetValue("Remarks");

