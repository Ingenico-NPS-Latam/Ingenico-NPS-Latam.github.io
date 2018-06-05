ComplexElement airlineDetails = response.getComplexElement("AirlineDetails");

fmt.Printf(airlineDetails.Name)

values := airlineDetails.Values
fmt.Printf(values.PNR)

legs := values.Legs

legs1 := legs.Items[1];
fmt.Printf(legs1.DepartureAirport)
fmt.Printf(legs1.DepartureDatetime)
fmt.Printf(legs1.DepartureAirportTimezone)
fmt.Printf(legs1.ArrivalAirport)
fmt.Printf(legs1.CarrierCode)
fmt.Printf(legs1.FlightNumber)
fmt.Printf(legs1.FareBasisCode)
fmt.Printf(legs1.FareClassCode)
fmt.Printf(legs1.BaseFare)
fmt.Printf(legs1.BaseFareCurrency)



passengers := values.Passengers

passengers1 := passengers.Items[1];
fmt.Printf(passengers1.FirstName)
fmt.Printf(passengers1.LastName)
fmt.Printf(passengers1.MiddleName)
fmt.Printf(passengers1.Type)
fmt.Printf(passengers1.DateOfBirth)
fmt.Printf(passengers1.Nationality)
fmt.Printf(passengers1.IDNumber)
fmt.Printf(passengers1.IDType)
fmt.Printf(passengers1.IDCountry)
fmt.Printf(passengers1.LoyaltyNumber)
fmt.Printf(passengers1.LoyaltyTier)



ticket := values.Ticket
fmt.Printf(ticket.TicketNumber)
fmt.Printf(ticket.Eticket)
fmt.Printf(ticket.Restricted)

issue := Ticket.Issue
fmt.Printf(issue.CarrierCode)
fmt.Printf(issue.TravelAgentCode)
fmt.Printf(issue.TravelAgentName)
fmt.Printf(issue.Date)
fmt.Printf(issue.Country)
fmt.Printf(issue.City)
fmt.Printf(issue.Address)

fmt.Printf(ticket.TotalFareAmount)
fmt.Printf(ticket.TotalTaxAmount)
fmt.Printf(ticket.TotalFeeAmount)


