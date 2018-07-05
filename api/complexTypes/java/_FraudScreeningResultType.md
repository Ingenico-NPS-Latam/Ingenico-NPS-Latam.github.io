import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement fraudScreeningResult = response.getComplexElement("FraudScreeningResult");

fraudScreeningResult.getValue("ResultCode");
fraudScreeningResult.getValue("ResultDescription");
fraudScreeningResult.getValue("AdditionalInfo");
