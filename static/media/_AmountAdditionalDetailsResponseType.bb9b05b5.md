$pspAmountAdditionalDetails = $response["psp_AmountAdditionalDetails"];
$pspAmountAdditionalDetails["Tip"];
$pspAmountAdditionalDetails["Discount"];

$taxes0 = $pspAmountAdditionalDetails["Taxes"][0];

$taxes0["TypeId"];
$taxes0["TypeDescription"];
$taxes0["Amount"];
$taxes0["Rate"];
$taxes0["BaseAmount"];

$appliedAmount = $taxes0["AppliedAmount"];


$remarks = $taxes0["Remarks"];


$taxes1 = $pspAmountAdditionalDetails["Taxes"][1];

$taxes1["TypeId"];
$taxes1["TypeDescription"];
$taxes1["Amount"];
$taxes1["Rate"];
$taxes1["BaseAmount"];

$appliedAmount = $taxes1["AppliedAmount"];


$remarks = $taxes1["Remarks"];