nps.getIIDetails("424242",
    methodResponse:{( methodResponse: NpsGetIINDetailsResponse?, error: Error?) -> Void in
        if error == nil{
            print(methodResponse?.responseCod as Any)
            print(methodResponse?.responseMsg as Any)
            print(methodResponse?.merchandId as Any)
            print(methodResponse?.product as Any)
            print(methodResponse?.posDateTime as Any)
        }
    })
