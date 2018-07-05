ComplexElement leg = response.getComplexElement("Leg");


leg := leg.Leg
fmt.Printf(leg.DepartureAirport)
fmt.Printf(leg.DepartureDatetime)
fmt.Printf(leg.DepartureAirportTimezone)
fmt.Printf(leg.ArrivalAirport)
fmt.Printf(leg.CarrierCode)
fmt.Printf(leg.FlightNumber)
fmt.Printf(leg.FareBasisCode)
fmt.Printf(leg.FareClassCode)
fmt.Printf(leg.BaseFare)
fmt.Printf(leg.BaseFareCurrency)

