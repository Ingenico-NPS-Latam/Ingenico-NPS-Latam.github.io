package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

QueryTxs := nps.NewRequerimientoStruct_QueryTxs()

QueryTxs.Psp_Version = "2.2"
QueryTxs.Psp_MerchantId = "sdk_test"
QueryTxs.Psp_QueryCriteria = "O"
QueryTxs.Psp_QueryCriteriaId = "ORDER69461-3"
QueryTxs.Psp_PosDateTime = "2019-12-01 12:00:00"

response, err := service.QueryTxs(QueryTxs)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



