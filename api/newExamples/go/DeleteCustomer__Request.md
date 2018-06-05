package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

DeleteCustomer := nps.NewRequerimientoStruct_DeleteCustomer()

DeleteCustomer.Psp_Version = "2.2"
DeleteCustomer.Psp_MerchantId = "sdk_test"
DeleteCustomer.Psp_CustomerId = "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b"
DeleteCustomer.Psp_PosDateTime = "2008-01-12 13:05:00"

response, err := service.DeleteCustomer(DeleteCustomer)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



