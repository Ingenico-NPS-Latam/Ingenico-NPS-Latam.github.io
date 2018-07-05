resp = nps.taxesResponseType.md(taxesResponseType.md)


local taxesResponse = resp.TaxesResponse
print(taxesResponse.TypeId)
print(taxesResponse.TypeDescription)
print(taxesResponse.Amount)
print(taxesResponse.Rate)
print(taxesResponse.BaseAmount)
print(taxesResponse.AppliedAmount)
print(taxesResponse.Remarks)

