using System;
using NpsSDK;

ComplexElement CardInputDetails = response.GetComplexElement("CardInputDetails");

cardInputDetails.GetValue("Number");
cardInputDetails.GetValue("ExpirationDate");
cardInputDetails.GetValue("SecurityCode");
cardInputDetails.GetValue("HolderName");
