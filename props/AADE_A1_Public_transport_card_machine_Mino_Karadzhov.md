# Analysis & Design: Assignment 1 
## Public transport card Machine
### Solution by Mino Karadzhov


### Use cases
* Obtain a new anonymous card
* Recharge a card
* Activate a choice day

<hr>

### Use case Descriptions

Name | Obtain a new anonymous card.
----|----
**Actor**|Treveller 
**Description**|A traveller wants to obtain a new anonymous card for the public transport services.
**Precondition**|Actor has a Contactless Bank card.
**Scenario**| Step 1. System displays homepage. <br> Step 2. Actor selects an option to obtain a new anonymous card. <br> Step 3. System requests Actor to enter an amount of money, that is going to be added to the card's balance. <br> Step 4. Actor enters an amount for the inital charge. <br> Step 5. System asks Actor to confirm their choice. <br> Step 6. Actor confirms their choice of amount.<br> Step 7. System asks Actor to place their Bank card on the Payment terminal. <br> Step 8. Actor places their Bank Card to the Terminal <br> Step 9. System shows a Message, that the payment was sucessfull. <br> Step 10. System ejects the Anonymous card.
**Result**|Actor has sucesfully purchased a new Anonymous Public Transport card. 
**Exceptions**|4a. System displays a message that the entered amount is invalid. <br>   4a.1. Returns to Step 3. <br> 8a. System Displays a message, that the Payment was not sucesfull. <br>   8a.1. Use-case ends here.
**Extensions**| 5a. Actor selects an option to correct the inital charged amount. <br>  1. Returns to step 3.

<br>
<hr>
<br>

Name | Recharge a card
----|----
**Actor**|Treveller 
**Description**|A Traveller tops their Card Balance with a value of their choice.
**Precondition**|Actor has a pre-obtained Public Transport Card.
**Scenario**| Step 1. System displays the Homepage. <br> Step 2. Actor Selects an option to charge their card. <br> Step 3. System asks Actor to insert their Public Transport Card. <br>Step 4. Actor inserts their Public Transport Card <br> Step 5. System asks Actor to enter an ammount, that they want to add to their Card Balance. <br> Step 6. Actor enters the desired ammount. <br> Step 7. System asks Actor to confirm the entered amount. <br> Step 8. Actor confirms the desired amount. <br> Step 9. System asks Actor to place their Bank card, next to the Payment terminal <br> Step 10. Actor places their card and makes the Payment <br> Step 11. System displays a Message, that the amount was added to the Balance and the payment was sucessfull.<br>
**Result**|The Traveller has added funds to their Public transport card balance.
**Exceptions**| 4a. System displays a message, that the card cannot be read. <br>   4a.1. Returns to Step 3. <br> 6a. System displays a message, that the entered amount is invalid. <br>  6a.1. Returns to Step 5. <br> 10a. System displays a message, that the payment was not sucessfull. <br>  10a.1. Use-case ends here.
**Extensions**| 8a. Actor selects an option to make a Correction on the desired ammount. <br>   1. Returns to Step 5. <br>

<br>
<hr>
<br>

Name | Activate a choice day
----|----
**Actor**|Traveller
**Description**|A traveller tries to select a choice day, when they will be able to travel for free, outside of peak hours.
**Precondition**|Actor has a pre-obtained personal public transport card and he/she is older than 60.
**Scenario**| Step 1. System displays homepage. <br> Step 2. Actor selects an option to Activate a choice day. <br> Step 3. System requests Actor to insert their Personal Public Transport card. <br> Step 4. Actor inserts their card. <br> Step 5. System asks Actor to select a choice day. <br> Step 6. Actor makes their Selection <br> Step 7. System asks Actor to confirm their selection <br> Step 8. Actor confirms their decision <br> Step 9. System displays a message, that the change was sucessfull.
**Result**|The Traveller has sucessfully selected a choice day. 
**Exceptions**|4a. System displays a message, that the card cannot be read by the device <br> 3a.1. Use-case ends here. <br> 4b. System displays a message that a change is not possible, because the traveller has already changed their choice day 7 times for the period of 1 year. <br> 4b.1. Use-case ends here.

<br>
<hr>
<hr>

## Use-case Diagram
![Use-case Diagram](https://github.com/FontysVenlo/aade-2020-assignments-aade-2020-g04/blob/master/assignment1/Public_Transport_card_Machine_Use_case_Mino_Karadzhov.svg)

<br>
<hr>

## Domain Model
![Domain Model](https://github.com/FontysVenlo/aade-2020-assignments-aade-2020-g04/blob/master/assignment1/Public_transport_card_machine_Domain_model_Mino_Karadzhov.svg)