package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

RecachePaymentMethodToken := nps.NewRequerimientoStruct_RecachePaymentMethodToken()

RecachePaymentMethodToken.Psp_Version = "2.2"
RecachePaymentMethodToken.Psp_MerchantId = "sdk_test"
RecachePaymentMethodToken.Psp_PaymentMethodId = "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE"
RecachePaymentMethodToken.Psp_CardSecurityCode = "123"

pspPerson := nps.NewPersonStruct()
pspPerson.FirstName = "John"
pspPerson.DateOfBirth = "1979-01-12"
pspPerson.LastName = "Doe"
pspPerson.MiddleName = "Michael"
pspPerson.PhoneNumber1 = "+1 011 11111111"
pspPerson.PhoneNumber2 = "+1 011 22222222"
pspPerson.Gender = "M"
pspPerson.Nationality = "ARG"
pspPerson.IDNumber = "54111111"
pspPerson.IDType = "200"

RecachePaymentMethodToken.psp_Person = pspPerson

pspAddress := nps.NewAddressStruct()
pspAddress.Street = "Av. Collins"
pspAddress.HouseNumber = "4702"
pspAddress.AdditionalInfo = "2 A"
pspAddress.City = "Buenos Aires"
pspAddress.StateProvince = "CABA"
pspAddress.Country = "ARG"
pspAddress.ZipCode = "1425"

RecachePaymentMethodToken.psp_Address = pspAddress
RecachePaymentMethodToken.Psp_ClientSession = "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs"

response, err := service.RecachePaymentMethodToken(RecachePaymentMethodToken)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



