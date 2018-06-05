ArrayList<InstallmentOption>() installments = nps.getInstallmentsOptions('8T3BOsXaLMxVsvtHiSuWKL1DEOUUDq3N', '14', '3');

for(InstallmentOption installment : installments) {
    Log.d("Nps", installment.getNumPayments());
    Log.d("Nps", installment.getInstallmentAmount());
}