package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

QueryCardNumber := nps.NewRequerimientoStruct_QueryCardNumber()

QueryCardNumber.Psp_Version = "1"
QueryCardNumber.Psp_MerchantId = "sdk_test"
QueryCardNumber.Psp_QueryCriteria = "T"
QueryCardNumber.Psp_QueryCriteriaId = "76577"
QueryCardNumber.Psp_PosDateTime = "2019-12-01 12:00:00"

response, err := service.QueryCardNumber(QueryCardNumber)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



