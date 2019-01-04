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

CreateCustomer := npsSdk.NewRequerimientoStruct_CreateCustomer()

CreateCustomer.Psp_Version = "2.2"
CreateCustomer.Psp_MerchantId = "sdk_test"
CreateCustomer.Psp_EmailAddress = "jhon.doe@example.com"
CreateCustomer.Psp_AlternativeEmailAddress = "jdoe@example.com"
CreateCustomer.Psp_AccountID = "jdoe78"
CreateCustomer.Psp_AccountCreatedAt = "2010-10-23"

pspPerson := nps.NewPersonStruct()
pspPerson.FirstName = "John"
pspPerson.LastName = "Doe"
pspPerson.MiddleName = "Michael"
pspPerson.PhoneNumber1 = "+1 011 11111111"
pspPerson.PhoneNumber2 = "+1 011 22222222"
pspPerson.DateOfBirth = "1979-01-12"
pspPerson.Gender = "M"
pspPerson.Nationality = "ARG"
pspPerson.IDNumber = "54111111"
pspPerson.IDType = "200"

CreateCustomer.psp_Person = pspPerson

pspAddress := nps.NewAddressStruct()
pspAddress.Street = "Av. Collins"
pspAddress.HouseNumber = "1245"
pspAddress.AdditionalInfo = "2 A"
pspAddress.StateProvince = "Florida"
pspAddress.City = "Miami"
pspAddress.Country = "USA"
pspAddress.ZipCode = "33140"

CreateCustomer.psp_Address = pspAddress

pspPaymentMethod := nps.NewPaymentMethodStruct()
pspPaymentMethod.PaymentMethodToken = "KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM"

Address := nps.NewAddressStruct()
Address.Street = "Av. Collins"
Address.HouseNumber = "1245"
Address.AdditionalInfo = "2 A"
Address.StateProvince = "Florida"
Address.City = "Miami"
Address.Country = "USA"
Address.ZipCode = "33140"

pspPaymentMethod.Address = Address

Person := nps.NewPersonStruct()
Person.FirstName = "John"
Person.LastName = "Doe"
Person.MiddleName = "Michael"
Person.PhoneNumber1 = "+1 011 11111111"
Person.PhoneNumber2 = "+1 011 22222222"
Person.DateOfBirth = "1979-01-12"
Person.Gender = "M"
Person.Nationality = "ARG"
Person.IDNumber = "54111111"
Person.IDType = "200"

pspPaymentMethod.Person = Person

CreateCustomer.psp_PaymentMethod = pspPaymentMethod
CreateCustomer.Psp_PosDateTime = "2008-01-12 13:05:00"

resp, err := service.CreateCustomer(CreateCustomer)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
