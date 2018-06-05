ComplexElement airlineTicket = response.getComplexElement("AirlineTicket");

print(airlineTicket.TicketNumber)
print(airlineTicket.Eticket)
print(airlineTicket.Restricted)

local issue = airlineTicket.Issue
print(issue.CarrierCode)
print(issue.TravelAgentCode)
print(issue.TravelAgentName)
print(issue.Date)
print(issue.Country)
print(issue.City)
print(issue.Address)

print(airlineTicket.TotalFareAmount)
print(airlineTicket.TotalTaxAmount)
print(airlineTicket.TotalFeeAmount)
