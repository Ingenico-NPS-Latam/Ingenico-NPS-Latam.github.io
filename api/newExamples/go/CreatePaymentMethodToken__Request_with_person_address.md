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

CreatePaymentMethodToken := npsSdk.NewRequerimientoStruct_CreatePaymentMethodToken()

CreatePaymentMethodToken.Psp_Version = "2.2"
CreatePaymentMethodToken.Psp_MerchantId = "sdk_test"

pspCardInputDetails := nps.NewCardInputDetailsStruct()
pspCardInputDetails.Number = "4507990000000010"
pspCardInputDetails.ExpirationDate = "2501"
pspCardInputDetails.SecurityCode = "123"
pspCardInputDetails.HolderName = "JOHN DOE"

CreatePaymentMethodToken.psp_CardInputDetails = pspCardInputDetails

pspPerson := nps.NewPersonStruct()
pspPerson.FirstName = "John"
pspPerson.LastName = "Doe"
pspPerson.MiddleName = "Michael"
pspPerson.DateOfBirth = "1979-01-12"
pspPerson.PhoneNumber1 = "+1 011 11111111"
pspPerson.PhoneNumber2 = "+1 011 22222222"
pspPerson.Gender = "M"
pspPerson.Nationality = "ARG"
pspPerson.IDNumber = "54111111"
pspPerson.IDType = "200"

CreatePaymentMethodToken.psp_Person = pspPerson

pspAddress := nps.NewAddressStruct()
pspAddress.Street = "Av. Collins"
pspAddress.HouseNumber = "4702"
pspAddress.AdditionalInfo = "2 A"
pspAddress.City = "Buenos Aires"
pspAddress.StateProvince = "CABA"
pspAddress.Country = "ARG"
pspAddress.ZipCode = "1425"

CreatePaymentMethodToken.psp_Address = pspAddress
CreatePaymentMethodToken.Psp_ClientSession = "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs"

resp, err := service.CreatePaymentMethodToken(CreatePaymentMethodToken)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
