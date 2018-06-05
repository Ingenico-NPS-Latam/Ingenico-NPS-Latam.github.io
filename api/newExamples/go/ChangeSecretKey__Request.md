package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

ChangeSecretKey := nps.NewRequerimientoStruct_ChangeSecretKey()

ChangeSecretKey.Psp_Version = "2.2"
ChangeSecretKey.Psp_MerchantId = "sdk_test"
ChangeSecretKey.Psp_NewSecretKey = "YOUR_NEW_SECRET_KEY"
ChangeSecretKey.Psp_PosDateTime = "2019-12-01 12:00:00"

response, err := service.ChangeSecretKey(ChangeSecretKey)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



