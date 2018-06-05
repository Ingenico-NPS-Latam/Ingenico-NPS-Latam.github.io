package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

GetIINDetails := nps.NewRequerimientoStruct_GetIINDetails()

GetIINDetails.Psp_Version = "2.2"
GetIINDetails.Psp_MerchantId = "sdk_test"
GetIINDetails.Psp_IIN = "424242"
GetIINDetails.Psp_PosDateTime = "2019-12-01 12:00:00"

response, err := service.GetIINDetails(GetIINDetails)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



