ComplexElement cardInputDetails = response.getComplexElement("CardInputDetails");

fmt.Printf(cardInputDetails.Number)
fmt.Printf(cardInputDetails.ExpirationDate)
fmt.Printf(cardInputDetails.SecurityCode)
fmt.Printf(cardInputDetails.HolderName)
