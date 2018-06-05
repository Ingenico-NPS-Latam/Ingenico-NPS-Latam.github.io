package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

QueryCardDetails := nps.NewRequerimientoStruct_QueryCardDetails()

QueryCardDetails.Psp_Version = "2.2"
QueryCardDetails.Psp_MerchantId = "psp_test"
QueryCardDetails.Psp_QueryCriteria = "T"
QueryCardDetails.Psp_QueryCriteriaId = "159744"
QueryCardDetails.Psp_PosDateTime = "2019-12-01 12:00:00"

resp, err := service.QueryCardDetails(QueryCardDetails)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



