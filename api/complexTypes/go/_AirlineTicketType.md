ComplexElement airlineTicket = response.getComplexElement("AirlineTicket");

fmt.Printf(airlineTicket.TicketNumber)
fmt.Printf(airlineTicket.Eticket)
fmt.Printf(airlineTicket.Restricted)

issue := airlineTicket.Issue
fmt.Printf(issue.CarrierCode)
fmt.Printf(issue.TravelAgentCode)
fmt.Printf(issue.TravelAgentName)
fmt.Printf(issue.Date)
fmt.Printf(issue.Country)
fmt.Printf(issue.City)
fmt.Printf(issue.Address)

fmt.Printf(airlineTicket.TotalFareAmount)
fmt.Printf(airlineTicket.TotalTaxAmount)
fmt.Printf(airlineTicket.TotalFeeAmount)
