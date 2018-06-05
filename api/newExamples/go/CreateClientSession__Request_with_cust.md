package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

CreateClientSession := nps.NewRequerimientoStruct_CreateClientSession()

CreateClientSession.Psp_Version = "2.2"
CreateClientSession.Psp_MerchantId = "sdk_test"
CreateClientSession.Psp_PosDateTime = "2019-12-01 12:00:00"
CreateClientSession.Psp_CustomerId = "K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f"

response, err := service.CreateClientSession(CreateClientSession)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



