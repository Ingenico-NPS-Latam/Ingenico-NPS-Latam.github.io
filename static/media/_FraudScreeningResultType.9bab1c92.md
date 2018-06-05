ComplexElement fraudScreeningResult = response.getComplexElement("FraudScreeningResult");

fmt.Printf(fraudScreeningResult.ResultCode)
fmt.Printf(fraudScreeningResult.ResultDescription)
fmt.Printf(fraudScreeningResult.AdditionalInfo)
