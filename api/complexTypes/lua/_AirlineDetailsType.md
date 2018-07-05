ComplexElement airlineDetails = response.getComplexElement("AirlineDetails");

print(airlineDetails.name)

local values = airlineDetails.values
print(values.PNR)

local legs = values.Legs

locallegs1 := legs[1]
print(legs1.DepartureAirport)
print(legs1.DepartureDatetime)
print(legs1.DepartureAirportTimezone)
print(legs1.ArrivalAirport)
print(legs1.CarrierCode)
print(legs1.FlightNumber)
print(legs1.FareBasisCode)
print(legs1.FareClassCode)
print(legs1.BaseFare)
print(legs1.BaseFareCurrency)



local passengers = values.Passengers

localpassengers1 := passengers[1]
print(passengers1.FirstName)
print(passengers1.LastName)
print(passengers1.MiddleName)
print(passengers1.Type)
print(passengers1.DateOfBirth)
print(passengers1.Nationality)
print(passengers1.IDNumber)
print(passengers1.IDType)
print(passengers1.IDCountry)
print(passengers1.LoyaltyNumber)
print(passengers1.LoyaltyTier)



local ticket = values.Ticket
print(ticket.TicketNumber)
print(ticket.Eticket)
print(ticket.Restricted)

local issue = Ticket.Issue
print(issue.CarrierCode)
print(issue.TravelAgentCode)
print(issue.TravelAgentName)
print(issue.Date)
print(issue.Country)
print(issue.City)
print(issue.Address)

print(ticket.TotalFareAmount)
print(ticket.TotalTaxAmount)
print(ticket.TotalFeeAmount)


