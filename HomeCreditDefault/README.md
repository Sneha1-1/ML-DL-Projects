# a) Introduction 
      Banks manage the flow of money between people and businesses. They use the money 
      deposited in the banks by their customers (people/institutions) to offer loans to clients 
      (people/business/institutions).
      They charge an interest rate on the loans given and part of this interest rate is given to 
      the money depositors in the bank keeping the rest with itself. They also charge money
      for the various products they offer to the clients. These two are the basic source of 
      money input to the banks.
# b) Business problem
      As the banks working depends on the interest earned from the loans, it is of utmost 
      importance that the borrowers repay the loan timely else the banks will have to bear 
      huge loss. Therefore, it is important to calculate the risk associated with lending money 
      to a borrower. So that banks can make better informed decisions while lending money to 
      the borrowers.
      Terms:
      Credit risk: It is the risk of a counterparty defaulting on payment obligations. Credit risk 
      splits up in several "credit risk components" – Default risk, Migration risk, Exposure Risk,
      Loss given default, counter party risk.
      1. Default risk: It the risk that borrowers’ default, meaning that they fail to comply with 
      their obligations to service debt.
      2. Exposure Risk: Exposure commonly designates the magnitude of the amount 
      subject to risk. For a loan it would be equal to the amount due plus interest 
      accrued.
      3. LGD: the actual loss the bank bears in case of failure to make the repayments by 
      the borrower.
      4. Migration risk: The direct or indirect losses caused due to the internal/external 
      ratings downgrade/upgrade as well as those may arise from credit migration event.
      We will be looking at the credit default risk for this problem statement.
      Objective: To predict if the borrower will default on the loan repayments.
# c) ML formulation of the business problem
      There are various factors in determining the credit risk of a borrower:
      1. Probability of default: probability that borrower will not be able to make timely 
      payments of installments
      2. Loss given default: loss that bank may have to bear in case the borrower goes 
      bankrupt
      These are calculated manually by the banks for every loan application and then the 
      decision to lend money is made.
      We need to automate this process using machine learning models by looking at the 
      various parameters from history of loans of the borrower.
# d) Business constraints
      1. No low latency requirements (10 sec to 2 mins is also fine)
      2. Very low error: As errors can be costly (example a borrower is given 1MUSD and he 
      defaults the bank can go bankrupt also. So errors can become very costly for the 
      banks)
# e) Data set column analysis:
      File: application_data.csv
      Total 122 columns which are divided into below subcategories 
      1. Personal Details
      2. Asset Details
      3. Credit Bureau Details
      4. Document submitted flags
      5. External Details
      6. Family Details
      7. Identification ids
      8. Loan Details
      9. Region Details (details of region where the borrower lives and works etc)
      10. Surrounding Details (how many borrowers in his surrounding region have defaulted 
      and such information)
      11. Target Variable: (1 - client with payment difficulties: he/she had late payment more 
      than X days on at least one of the first Y installments of the loan in our sample, 0 - all 
      other cases)
      File: previous_application_data.csv
      Total 38 columns which are divided into below subcategories
      1. Personal Details
      2. Loan Details
      3. Identification ids.
      Other files: Installation, Bureau, Bureau_balance, POS_CASH_balance, credit_card_balance.
      
# f) Performance metric:
      1. AUC score 


