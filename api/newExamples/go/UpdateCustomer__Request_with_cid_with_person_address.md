package main

import (
    "fmt"
    "github.com/Ingenico-NPS-Latam/nps-sdk-go/npsSdk"
    CONSTANTS "github.com/Ingenico-NPS-Latam/nps-sdk-go/npsSdk/constants"
)

func main() {

err := npsSdk.Configure(map[string]interface{}(
    "environment": CONSTANTS.SANDBOX_ENV,
    "secret_key": "_YOUR_SECRET_KEY_",
    "debug": true,
    "log_level": CONSTANTS.DEBUG,
})

service := npsSdk.NewPaymentServicePlatformPortType(true)

UpdateCustomer := npsSdk.NewRequerimientoStruct_UpdateCustomer()

UpdateCustomer.Psp_Version = "2.2"
UpdateCustomer.Psp_MerchantId = "sdk_test"
UpdateCustomer.Psp_CustomerId = "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b"
UpdateCustomer.Psp_EmailAddress = "jhon.doe@example.com"
UpdateCustomer.Psp_AlternativeEmailAddress = "jdoe@example.com"
UpdateCustomer.Psp_AccountCreatedAt = "2010-10-23"
UpdateCustomer.Psp_AccountID = "jdoe78"

pspPerson := nps.NewPersonStruct()
pspPerson.FirstName = "John"
pspPerson.LastName = "Doe"
pspPerson.MiddleName = "Michael"
pspPerson.PhoneNumber1 = "+1 011 11111111"
pspPerson.PhoneNumber2 = "+1 011 22222222"
pspPerson.Gender = "M"
pspPerson.DateOfBirth = "1979-01-12"
pspPerson.Nationality = "ARG"
pspPerson.IDNumber = "54111111"
pspPerson.IDType = "200"

UpdateCustomer.psp_Person = pspPerson

pspAddress := nps.NewAddressStruct()
pspAddress.Street = "Av. Collins"
pspAddress.HouseNumber = "1245"
pspAddress.AdditionalInfo = "2 A"
pspAddress.City = "Miami"
pspAddress.StateProvince = "Florida"
pspAddress.Country = "USA"
pspAddress.ZipCode = "33140"

UpdateCustomer.psp_Address = pspAddress

pspPaymentMethod := nps.NewPaymentMethodStruct()

CardInputDetails := nps.NewCardInputDetailsStruct()
CardInputDetails.Number = "4507990000000010"
CardInputDetails.ExpirationDate = "2501"
CardInputDetails.SecurityCode = "123"
CardInputDetails.HolderName = "JOHN DOE"

pspPaymentMethod.CardInputDetails = CardInputDetails

Person := nps.NewPersonStruct()
Person.FirstName = "John"
Person.LastName = "Doe"
Person.MiddleName = "Michael"
Person.PhoneNumber1 = "+1 011 11111111"
Person.PhoneNumber2 = "+1 011 22222222"
Person.Gender = "M"
Person.DateOfBirth = "1979-01-12"
Person.Nationality = "ARG"
Person.IDNumber = "54111111"
Person.IDType = "200"

pspPaymentMethod.Person = Person

Address := nps.NewAddressStruct()
Address.Street = "Av. Collins"
Address.HouseNumber = "1245"
Address.AdditionalInfo = "2 A"
Address.City = "Miami"
Address.StateProvince = "Florida"
Address.Country = "USA"
Address.ZipCode = "33140"

pspPaymentMethod.Address = Address

UpdateCustomer.psp_PaymentMethod = pspPaymentMethod
UpdateCustomer.Psp_PosDateTime = "2008-01-12 13:05:00"

resp, err := service.UpdateCustomer(UpdateCustomer)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
