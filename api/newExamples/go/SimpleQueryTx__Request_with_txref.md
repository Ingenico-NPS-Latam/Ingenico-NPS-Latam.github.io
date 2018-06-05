package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

SimpleQueryTx := nps.NewRequerimientoStruct_SimpleQueryTx()

SimpleQueryTx.Psp_Version = "2.2"
SimpleQueryTx.Psp_MerchantId = "sdk_test"
SimpleQueryTx.Psp_QueryCriteria = "M"
SimpleQueryTx.Psp_QueryCriteriaId = "ORDER69461-3"
SimpleQueryTx.Psp_PosDateTime = "2019-12-01 12:00:00"

response, err := service.SimpleQueryTx(SimpleQueryTx)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



