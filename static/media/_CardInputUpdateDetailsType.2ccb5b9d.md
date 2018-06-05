using System;
using NpsSDK;

ComplexElement CardInputUpdateDetails = response.GetComplexElement("CardInputUpdateDetails");

cardInputUpdateDetails.GetValue("ExpirationDate");
cardInputUpdateDetails.GetValue("HolderName");
