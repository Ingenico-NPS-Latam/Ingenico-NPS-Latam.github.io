package main

import (
    "fmt"
    "github.com/Ingenico-NPS-Latam/nps-sdk-go/npsSdk"
    CONSTANTS "github.com/Ingenico-NPS-Latam/nps-sdk-go/npsSdk/constants"
)

func main() {

err := npsSdk.Configure(map[string]interface{}(
    "environment": CONSTANTS.SANDBOX_ENV,
    "secret_key": "_YOUR_SECRET_KEY_",
    "debug": true,
    "log_level": CONSTANTS.DEBUG,
})

service := npsSdk.NewPaymentServicePlatformPortType(true)

GetInstallmentsOptions := npsSdk.NewRequerimientoStruct_GetInstallmentsOptions()

GetInstallmentsOptions.Psp_Version = "2.2"
GetInstallmentsOptions.Psp_MerchantId = "sdk_test"
GetInstallmentsOptions.Psp_Amount = "100"
GetInstallmentsOptions.Psp_Product = "14"
GetInstallmentsOptions.Psp_Currency = "152"
GetInstallmentsOptions.Psp_Country = "CHL"
GetInstallmentsOptions.Psp_NumPayments = "12"
GetInstallmentsOptions.Psp_PaymentMethodToken = "KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM"
GetInstallmentsOptions.Psp_ClientSession = "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs"
GetInstallmentsOptions.Psp_PosDateTime = "2017-04-04 13:35:20"

resp, err := service.GetInstallmentsOptions(GetInstallmentsOptions)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
