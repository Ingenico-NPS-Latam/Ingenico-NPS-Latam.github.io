resp, err := service.taxesResponseType.md(taxesResponseType.md)


taxesResponse := resp.TaxesResponse
fmt.Printf(taxesResponse.TypeId)
fmt.Printf(taxesResponse.TypeDescription)
fmt.Printf(taxesResponse.Amount)
fmt.Printf(taxesResponse.Rate)
fmt.Printf(taxesResponse.BaseAmount)
fmt.Printf(taxesResponse.AppliedAmount)
fmt.Printf(taxesResponse.Remarks)

