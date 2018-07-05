using System;
using NpsSDK;

ComplexElement FraudScreeningResult = response.GetComplexElement("FraudScreeningResult");

fraudScreeningResult.GetValue("ResultCode");
fraudScreeningResult.GetValue("ResultDescription");
fraudScreeningResult.GetValue("AdditionalInfo");
