package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

FraudScreening := nps.NewRequerimientoStruct_FraudScreening()

FraudScreening.Psp_Version = "2.2"
FraudScreening.Psp_MerchantId = "sdk_test"
FraudScreening.Psp_TxSource = "WEB"
FraudScreening.Psp_MerchTxRef = "ORDER66666-3"
FraudScreening.Psp_MerchOrderId = "ORDER66666"
FraudScreening.Psp_Amount = "15050"
FraudScreening.Psp_NumPayments = "1"
FraudScreening.Psp_Currency = "032"
FraudScreening.Psp_Country = "ARG"
FraudScreening.Psp_Product = "14"
FraudScreening.Psp_CardNumber = "4507990000000010"
FraudScreening.Psp_CardExpDate = "1912"
FraudScreening.Psp_PosDateTime = "2019-12-01 12:00:00"

response, err := service.FraudScreening(FraudScreening)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



