use NpsPerlSDK::Nps;
use warnings;
use strict;

NpsPerlSDK::Configuration::configure( 
    environment => $constants::SANDBOX_ENV,
    secret_key => "_YOUR_SECRET_KEY_",
    sanitize => 1 
    );

my $params = {
    "psp_Version" => "2.2",
    "psp_MerchantId" => "sdk_test",
    "psp_TxSource" => "WEB",
    "psp_MerchTxRef" => "ORDER69461-3",
    "psp_MerchOrderId" => "ORDER69461",
    "psp_Amount" => "15050",
    "psp_NumPayments" => "1",
    "psp_Currency" => "032",
    "psp_Country" => "ARG",
    "psp_Product" => "14",
    "psp_CardNumber" => "4507990000000010",
    "psp_CardExpDate" => "1912",
    "psp_PosDateTime" => "2019-12-01 12:00:00",
    "psp_AirlineDetails" => {
        "PNR" => "154DDD54DWW11",
        "Legs" => [
            {
                "DepartureAirport" => "EZE",
                "DepartureDatetime" => "2014-05-12 13:05:00",
                "DepartureAirportTimezone" => "-03:00",
                "ArrivalAirport" => "AMS",
                "CarrierCode" => "KL",
                "FlightNumber" => "842",
                "FareBasisCode" => "HL7LNR",
                "FareClassCode" => "FR",
                "BaseFare" => "30000",
                "BaseFareCurrency" => "032",
            }
        ],
        "Passengers" => [
            {
                "FirstName" => "John",
                "LastName" => "Doe",
                "MiddleName" => "Michael",
                "Type" => "A",
                "DateOfBirth" => "1979-01-12",
                "Nationality" => "ARG",
                "IDNumber" => "54111111",
                "IDType" => "100",
                "IDCountry" => "ARG",
                "LoyaltyNumber" => "254587547",
                "LoyaltyTier" => "1",
            }
        ],
        "Ticket" => {
            "TicketNumber" => "07411865255578",
            "Eticket" => "1",
            "Restricted" => "1",
            "Issue" => {
                "TravelAgentCode" => "32165464",
                "TravelAgentName" => "Washington Hilton",
                "Date" => "2017-01-10",
                "Country" => "ARG",
                "City" => "Buenos Aires",
                "Address" => "Av. Rivadavia 1111",
                    },
            "TotalFareAmount" => "80000",
            "TotalTaxAmount" => "25200",
            "TotalFeeAmount" => "14800",
            }
    }
};

my $response = NpsPerlSDK::Nps::pay_online_2p($params);