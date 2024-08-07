# TSA_Account_closure

## *Check if the Data in the table is EOD yesterday*
    This can be checked from Balasubramani

    Step1: At line 11 change the date to D-1<br><br>
    Step2: At line around 36 (and (TSA_Opening_date < date '2023-10-18')   ####D-60 days(SHOULD BE SAME DATE FOR 1ST,2ND,3RD NOTIFICATION)) Change the date D-60 Days <br><br>
    Step3: At line around 45 (WHEN tsa_status = 'Active' and Last_TSA_EOD_Balance_Date is null and (TSA_Opening_date < date '2023-10-18')  ####D-60 days(SHOULD BE SAME DATE FOR 1ST,2ND,3RD NOTIFICATION)) Change the date D-60 Days <br><br>
    Step4: At line 58 (and TSA_Opening_date < date '2023-06-18'  and (Last_TSA_Credit_Date < date '2023-06-18' and Last_TSA_Debit_Date < date '2023-06-18' and coalesce(Last_Group_Stash_Credit_Date,date '1970-01-01') < date '2023-06-18')  ####D-180 days(SHOULD BE SAME DATE FOR 1ST,2ND,3RD NOTIFICATION)) <br><br>
    Step5: At line 72 (Run_Date = date '2024-01-09'###DATE change here to D-1) Change the date to D-1<br><br>
