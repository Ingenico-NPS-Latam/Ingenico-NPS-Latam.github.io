package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

SplitAuthorize3p := nps.NewRequerimientoStruct_SplitAuthorize_3p()

SplitAuthorize3p.Psp_Version = "2.2"
SplitAuthorize3p.Psp_MerchantId = "sdk_test"
SplitAuthorize3p.Psp_TxSource = "WEB"
SplitAuthorize3p.Psp_MerchOrderId = "ORDER66666"
SplitAuthorize3p.Psp_ReturnURL = "http://localhost/"
SplitAuthorize3p.Psp_FrmLanguage = "es_AR"
SplitAuthorize3p.Psp_Amount = "15050"
SplitAuthorize3p.Psp_Currency = "032"
SplitAuthorize3p.Psp_Country = "ARG"
SplitAuthorize3p.Psp_Product = "14"
SplitAuthorize3p.Psp_PosDateTime = "2019-12-01 12:00:00"

ComplexElementArray pspTransactions = new ComplexElementArray();

ComplexElementArrayItem pspTransactions1 = new ComplexElementArrayItem();
pspTransactions1.Psp_MerchantId = "sdk_test"
pspTransactions1.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions1.Psp_Product = "14"
pspTransactions1.Psp_Amount = "10000"
pspTransactions1.Psp_NumPayments = "1"

pspTransactions.add(pspTransactions1);

ComplexElementArrayItem pspTransactions2 = new ComplexElementArrayItem();
pspTransactions2.Psp_MerchantId = "psp_test"
pspTransactions2.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions2.Psp_Product = "14"
pspTransactions2.Psp_Amount = "5050"
pspTransactions2.Psp_NumPayments = "1"

pspTransactions.add(pspTransactions2);

SplitAuthorize3p.psp_Transactions = pspTransactions

response, err := service.SplitAuthorize_3p(SplitAuthorize3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



