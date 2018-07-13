RootElement data = new RootElement();


ComplexElement Passenger = new ComplexElement();
Passenger.add("FirstName", "John");
Passenger.add("LastName", "Doe");
Passenger.add("MiddleName", "Michael");
Passenger.add("Type", "A");
Passenger.add("DateOfBirth", "1979-01-12");
Passenger.add("Nationality", "ARG");
Passenger.add("IDNumber", "54111111");
Passenger.add("IDType", "100");
Passenger.add("IDCountry", "ARG");
Passenger.add("LoyaltyNumber", "254587547");
Passenger.add("LoyaltyTier", "1");

data.add("Passenger", Passenger);
