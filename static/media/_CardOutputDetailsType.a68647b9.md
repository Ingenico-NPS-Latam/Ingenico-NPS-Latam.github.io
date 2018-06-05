using System;
using NpsSDK;

ComplexElement CardOutputDetails = response.GetComplexElement("CardOutputDetails");

cardOutputDetails.GetValue("ExpirationDate");
cardOutputDetails.GetValue("ExpirationYear");
cardOutputDetails.GetValue("ExpirationMonth");
cardOutputDetails.GetValue("HolderName");
cardOutputDetails.GetValue("IIN");
cardOutputDetails.GetValue("Last4");
cardOutputDetails.GetValue("MaskedNumber");
cardOutputDetails.GetValue("MaskedNumberAlternative");
