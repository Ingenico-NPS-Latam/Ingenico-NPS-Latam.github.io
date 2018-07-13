RootElement data = new RootElement();


ComplexElement Passenger = new ComplexElement();
Passenger.Add("FirstName", "John");
Passenger.Add("LastName", "Doe");
Passenger.Add("MiddleName", "Michael");
Passenger.Add("Type", "A");
Passenger.Add("DateOfBirth", "1979-01-12");
Passenger.Add("Nationality", "ARG");
Passenger.Add("IDNumber", "54111111");
Passenger.Add("IDType", "100");
Passenger.Add("IDCountry", "ARG");
Passenger.Add("LoyaltyNumber", "254587547");
Passenger.Add("LoyaltyTier", "1");

data.Add("Passenger", Passenger);
