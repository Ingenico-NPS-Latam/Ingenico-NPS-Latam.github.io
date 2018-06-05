package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

UpdatePaymentMethod := nps.NewRequerimientoStruct_UpdatePaymentMethod()

UpdatePaymentMethod.Psp_Version = "2.2"
UpdatePaymentMethod.Psp_MerchantId = "sdk_test"
UpdatePaymentMethod.Psp_PaymentMethodId = "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE"
UpdatePaymentMethod.Psp_PaymentMethodTag = "Corporate card"

pspCardInputDetails := nps.NewCardInputDetailsStruct()
pspCardInputDetails.ExpirationDate = "2501"
pspCardInputDetails.HolderName = "JOHN DOE"

UpdatePaymentMethod.psp_CardInputDetails = pspCardInputDetails

pspPerson := nps.NewPersonStruct()
pspPerson.FirstName = "John"
pspPerson.LastName = "Doe"
pspPerson.MiddleName = "Michael"
pspPerson.PhoneNumber1 = "+1 011 11111111"
pspPerson.PhoneNumber2 = "+1 011 22222222"
pspPerson.DateOfBirth = "1979-01-12"
pspPerson.Nationality = "ARG"
pspPerson.Gender = "M"
pspPerson.IDNumber = "54111111"
pspPerson.IDType = "200"

UpdatePaymentMethod.psp_Person = pspPerson

pspAddress := nps.NewAddressStruct()
pspAddress.Street = "Av. Collins"
pspAddress.HouseNumber = "4702"
pspAddress.AdditionalInfo = "2 A"
pspAddress.StateProvince = "CABA"
pspAddress.City = "Buenos Aires"
pspAddress.Country = "ARG"
pspAddress.ZipCode = "1425"

UpdatePaymentMethod.psp_Address = pspAddress
UpdatePaymentMethod.Psp_PosDateTime = "2008-01-12 13:05:00"

response, err := service.UpdatePaymentMethod(UpdatePaymentMethod)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



