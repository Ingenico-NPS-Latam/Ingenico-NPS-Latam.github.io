using System;
using NpsSDK;

ComplexElement Passenger = response.GetComplexElement("Passenger");


ComplexElement passenger = Passenger.GetComplexElement("Passenger");
passenger.GetValue("FirstName");
passenger.GetValue("LastName");
passenger.GetValue("MiddleName");
passenger.GetValue("Type");
passenger.GetValue("DateOfBirth");
passenger.GetValue("Nationality");
passenger.GetValue("IDNumber");
passenger.GetValue("IDType");
passenger.GetValue("IDCountry");
passenger.GetValue("LoyaltyNumber");
passenger.GetValue("LoyaltyTier");

