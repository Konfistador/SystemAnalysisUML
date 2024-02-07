# ATM (Automatic Teller Machine)

## Introduction
This part of the repostiory, hosts UML artefacts, that analyse the business case of an ATM(Automatic Teller Machine) 

### Use cases
* Insert card and enter PIN code.
* Withdraw Money.
* Check Balance.
* Change PIN Code.


<hr>


### Use case descriptions

Name | Insert Card and Enter PIN code
----|----
**Actor**|Cardholder
**Description**|Cardholder inserts their card and enters their pincode, in order to use the ATM services.
**Precondition**|Actor has a pre-existing Bank account and a Bank card, associated with it.
**Scenario**| Step 1. Actor inserts their Bank card into the ATM <br> Step 2. System requests Actor to enter their PIN code. <br> Step 3. Actor enters their PIN code. <br> Step 4. Actor submits their PIN code to the System. <br>Step 5. System accepts the PIN code and presents the available services.
**Result**|Actor has sucesfully identified him/herself, so they can proceed with the other ATM services.
**Exceptions**|4a. System informs the Actor, that the entered PIN code is not correct. <br>   4a.1. ATM Ejects the card back. <br> 4a.2. Use-case ends here.


<hr>
<br>

Name | Withdraw Money
----|----
**Actor**|Card holder
**Description**|Card holder, wants to withdraw Cash from their Bank account, using their Bank card.
**Precondition**|Actor has a pre-existing Bank account and a Bank card, associated with it.
**Scenario**| Step 1. Actor <ins>Inserts their Card and enters their PIN code</ins>.<br> Step 2. Actor selects an option to Withdraw Money. <br> Step 3. System displays several pre-defined amounts and an option to manually Enter an amount of money to withdraw. <br> Step 4. Actor makes their choice of an amount to withdraw. <br> Step 5. Actor submits their choice. <br> Step 6. System asks Actor if they want a receipt. <br> Step 7. Actor chooses, weather to request a Receipt. <br> Step 8. System provides Actor with the selected Amount of Cash <br> Step 9. System returns the Bank Card to the Actor.
**Result**|Actor has sucesfully withdrawn an amount of cash, from their Bank account.
**Exceptions**|5a. System informs Actor, that the funds in their bank account are not sufficent for completing the operation. <br> 5a.1. System ejects the card.<br> 5a2. Use Case ends here.<br><br> 5b. System displays a message, that the custom entered amount is invalid. <br>  5b.1. Returns to Step 3.
**Extensions**|4a. Actor chooses one of the pre-defined amounts. <br> 1. System acknowledges the selected amount for the withdraw. Proceeds to Step 5.<br><br> 4b. Actor chooses to manually enter an amount for the withdraw. <br> 1. System asks Actor to enter the desired amount. <br> 2. Actor enters the amount, that they want to withdraw. <br> 3. System acknowledges the entered amount for the withdraw. Proceeds to Step 5. <br><br> 7a. Actor selects that they Do not want to receive a Receipt. <br> 1. System registers their choice. Proceeds to Step 8<br><br> 7b. Actor selects that they want to receive a Receipt. <br>    1. System provides Actor with a Receipt for the operation. Proceeds to Step 8.<br>


<hr>
<br>

Name | Check Balance
----|----
**Actor**|Cardholder
**Description**|Cardholder would like to check the Balance of their Bank account.
**Precondition**|Actor has a pre-excisting Bank account and a Bank card, associated with it.
**Scenario**| Step 1. Actor <ins>Inserts their Card and enters their PIN code</ins>.<br> Step 2. Actor selects an option to Check their Balance.<br> Step 3. System displays Actor's balance and their most recent withdraws. <br> 
**Result**|Actor sees their Balance and their most-recent withdraws.
**Exceptions**|2a. System informs Actor that the Balance information is not available, due to the fact that the Bank associated with the ATM is not associated with their Bank Card. <br> 1. Use-case ends here.

<br>
<hr>
<br>

Name | Change PIN code
----|----
**Actor**|Cardholder
**Description**|Cardholder wants to change their Bank card PIN code.
**Precondition**|Actor has a pre-existing Bank account with a Bank card, associated with it.
**Scenario**| Step 1. Actor <ins>Inserts their Card and enters their PIN code</ins>.<br> Step 2. Actor Selects an option to change their PIN code. <br> Step 3. System requests Actor to enter their new PIN code <br> Step 4. Actor enters their new PIN code. <br> Step 5. System requests Actor to confirm their new PIN code by entering it again. <br> Step 6. Actor confirms their new PIN code by entering it once again. <br> Step 7. System informs Actor, that their PIN code was sucesfully Changed.<br>
**Result**|Actor has sucessfuly changed their Bank card PIN code.
**Exceptions**|5a. System Dispalys a message, that the change was not sucessful, because the two New PIN codes did not match. <br>  1. Returns to Step 3.
