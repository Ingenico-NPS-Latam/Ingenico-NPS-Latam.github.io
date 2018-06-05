package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

CreatePaymentMethod := nps.NewRequerimientoStruct_CreatePaymentMethod()

CreatePaymentMethod.Psp_Version = "2.2"
CreatePaymentMethod.Psp_MerchantId = "sdk_test"
CreatePaymentMethod.Psp_CustomerId = "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b"

pspPaymentMethod := nps.NewPaymentMethodStruct()

CardInputDetails := nps.NewCardInputDetailsStruct()
CardInputDetails.Number = "4507990000000010"
CardInputDetails.ExpirationDate = "2501"
CardInputDetails.SecurityCode = "123"
CardInputDetails.HolderName = "JOHN DOE"

pspPaymentMethod.CardInputDetails = CardInputDetails
pspPaymentMethod.PaymentMethodTag = "Corporate card"

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

Address := nps.NewAddressStruct()
Address.Street = "Av. Collins"
Address.HouseNumber = "4702"
Address.AdditionalInfo = "2 A"
Address.City = "Buenos Aires"
Address.StateProvince = "CABA"
Address.Country = "ARG"
Address.ZipCode = "1425"

pspPaymentMethod.Address = Address

CreatePaymentMethod.psp_PaymentMethod = pspPaymentMethod
CreatePaymentMethod.Psp_SetAsCustomerDefault = "1"
CreatePaymentMethod.Psp_PosDateTime = "2008-01-12 13:05:00"

response, err := service.CreatePaymentMethod(CreatePaymentMethod)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



