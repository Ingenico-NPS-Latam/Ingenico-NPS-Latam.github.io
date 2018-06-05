package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

CreateCustomer := nps.NewRequerimientoStruct_CreateCustomer()

CreateCustomer.Psp_Version = "2.2"
CreateCustomer.Psp_MerchantId = "sdk_test"
CreateCustomer.Psp_EmailAddress = "jhon.doe@example.com"
CreateCustomer.Psp_AlternativeEmailAddress = "jdoe@example.com"
CreateCustomer.Psp_AccountID = "jdoe78"
CreateCustomer.Psp_AccountCreatedAt = "2010-10-23"

pspPaymentMethod := nps.NewPaymentMethodStruct()
pspPaymentMethod.PaymentMethodToken = "KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM"

CreateCustomer.psp_PaymentMethod = pspPaymentMethod
CreateCustomer.Psp_PosDateTime = "2008-01-12 13:05:00"

response, err := service.CreateCustomer(CreateCustomer)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



