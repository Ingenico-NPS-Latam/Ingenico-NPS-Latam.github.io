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

PayOnLine3p := npsSdk.NewRequerimientoStruct_PayOnLine_3p()

PayOnLine3p.Psp_Version = "2.2"
PayOnLine3p.Psp_MerchantId = "sdk_test"
PayOnLine3p.Psp_TxSource = "WEB"
PayOnLine3p.Psp_MerchTxRef = "ORDER76666-3"
PayOnLine3p.Psp_MerchOrderId = "ORDER76666"
PayOnLine3p.Psp_ReturnURL = "http://localhost/"
PayOnLine3p.Psp_FrmLanguage = "es_AR"
PayOnLine3p.Psp_Amount = "1200000"
PayOnLine3p.Psp_NumPayments = "1"
PayOnLine3p.Psp_Currency = "986"
PayOnLine3p.Psp_Country = "BRA"
PayOnLine3p.Psp_Product = "14"
PayOnLine3p.Psp_PosDateTime = "2019-12-01 12:00:00"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsRequestStruct()
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes := nps.NewArrayOf_TaxesRequestStruct()
Taxes.Items = make([]*nps.NewTaxesRequestStruct(), 0)

Taxes1 := nps.NewTaxesRequestStruct()
Taxes1.TypeId = "100"
Taxes1.Amount = "200000"
Taxes.Items = append(Taxes.Items, Taxes1)


PayOnLine3p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

resp, err := service.PayOnLine_3p(PayOnLine3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
