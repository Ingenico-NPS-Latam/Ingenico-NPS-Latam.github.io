ComplexElement leg = response.getComplexElement("Leg");


local leg = leg.Leg
print(leg.DepartureAirport)
print(leg.DepartureDatetime)
print(leg.DepartureAirportTimezone)
print(leg.ArrivalAirport)
print(leg.CarrierCode)
print(leg.FlightNumber)
print(leg.FareBasisCode)
print(leg.FareClassCode)
print(leg.BaseFare)
print(leg.BaseFareCurrency)

