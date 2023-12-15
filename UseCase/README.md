# Use-case Descriptions and Diagrams

## About the technique:
Use cases are a technique for capturing the functional requirements of a system. The idea is to provide a narrative of how a system is being used by describing the typical interactions between the users of a system and a system itself.
Use cases are essential in understanding user requirements and ensuring the developed system meets these needs. They are also a cornerstone in user-centric design and agile methodologies.

## Few words on the Artefacts in this directory
The following artefacts are results of analysis on several pre-defined business cases. Their goal is to provide an understanding of what the system is expected to do, when a given scenario with expected results takes place.

## Business cases

### ATM(Automated teller machine)
Before a user can select a transaction, they have to insert their bank card and enter the correct pin-code. The ATM offers three transactions: withdraw money, check balance, change pin code. Checking the balance is only possible when the bank associated with the card is the same as the bank associated with the ATM. A bank card is always associated with one current account. When checking a balance, customers can also see their most recent withdrawals.

[UseCaseDiagram](https://raw.githubusercontent.com/Konfistador/SystemAnalysisUML/b150b09b292dba59fd6e6280e564f6dfa4a57563/UseCase/Diagram/atmUseCaseD.svg)
![atmUseCaseD](https://github.com/Konfistador/SystemAnalysisUML/assets/15638687/c50ff3b6-8034-4b40-bcfe-f43f0f7df25e)
#### Use case Descriptions

* Insert card and enter PIN code.
* Withdraw Money.
* Check Balance.
* Change PIN Code.


<hr>


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

<br>

### Music streaming service

We are being asked to analyze requirements for a mobile app that offers a music streaming service. If you start the app, users are requested to sign in, before they can search music, play music and create, edit or view personal playlists. The music streaming service registers each play of a song, making it possible to show the number of plays a certain song has across all users (e.g. when the results of a search are shown). Furthermore, the app can show lists of personal top played songs and of country-specific top played songs.

#### Use cases
* Sign in.
* Register.
* Search for a song, type of music.
* Play a song.
* Create playlist.
* Add songs to a playlist.
* Remove songs from a playlist.
* Add songs to a playlist.
* Delete playlist.
* Rename playlist.
* View Playlist.
* View personal top-played songs.
* View country-specific top-played songs.
* View number of plays of a specific song.

<hr>



Name | Sign in
----|----
**Actor**|Registered User
**Description**|A Registered user signs into their account, as they start the Application.
**Precondition**|The Actor already has a registraion in the app.
**Scenario**| Step 1. Application asks Actor for their log-in credentials. <br> Step 2. Actor enters their log-in credentials. <br> Step 3. Application displays Actor's homepage.
**Result**|Actor is signed-in into his/her account.
**Exceptions**| 2. Application Displays a message for an Incorrect Log-in Credentials. <br> 2.1 Use-case ends here.
**Extentions**| None
<br>
<hr>

Name | Register
----|----
**Actor**|Unregistered Guest
**Description**|An Unregistered user, creates an account in the Music Application.
**Precondition**|None
**Scenario**| Step 1. Actor selects an option for creating a new account. <br> Step 2. Application asks Actor for information, required for creating an account.<br> Step 3. Actor enters the required information. <br> Step 4. Actor submits the entered information. <br> Step 5. Application informs Actor that the registration was sucessfull.  
**Result**|Actor has created a new User Account in the application.
**Exceptions**|4. Application informs Actor that the Entered information is invalid. <br> 4.1 Return to step 2
<br>
<hr>

Name | Search for Music
----|----
**Actor**|Registered User
**Description**|User of the application searches for a certain Music and user is Signed-in into their Account
**Precondition**|Actor is signed-in into their pre-existing User Profile.
**Scenario**| Step 1. Actor selects an option for searching for Music. <br> Step 2. Application asks Actor to enter criteria for the search <br> Step 3. Actor enters criteria for the Music search <br> Step 4. Actor submits the criterias <br> Step 5. Application displays Results from the Search.
**Result**|Actor is provided with the results of their search for Music, according to a their given criteria.
**Exceptions**|4a. Application informs the actor, that they have entered an invalid search criteria. <br> 4a.1. Return to Step 2. <br> 4b. Application informs actor, that there are no results, according to the provided search criterias. <br> 4b.1. Return to Step 2.
**Extensions#**|3a. Actors enters part of song's lyrics <br>    1. Actor submits lyrics as a search criteria. Returns to step 4.<br> 3b. Actor enters song's name <br>      1. Actor submits song's name as a search criteria. Returns to step 4. <br> 3c. Actor enters name of a Musical Genre as a search criteria. <br>      1. Actor submits Genre's name as a criteria of search. Return to step 4. <br> 3d. Actor enters name of an artist <br>       1. Actor submits name of a Musical Artist as a search criteria. Return to step 4. <br> 3e. Actor enters name of an album. <br>      1. Actor enters name of an album as a search criteria. Return to step 4. <br> 3e. Actor enters personal top-played songs as a search criteria <br>  1. User <ins>Views their personal most-played songs</ins> <br> 3f. Actor enters contry - specific top-played songs as a search criteria<br>        1. User <ins>views the country-specific top played songs</ins>.
<br>

<hr>

Name | Play a song
----|----
**Actor**|Registered User
**Description**|User plays a song
**Precondition**|Actor is signed-in into a pre-existing User Account and there is music available to play.
**Scenario**| Step 1. Application displays a variety of songs. <br> Step 2. Actor selects a song. <br> Step 3. Application shows variety of options for the selected song. <br> Step 4. Actor selects to play the song. <br> Step 5. Application plays the selected song.
**Result**|User listens to a song of their choice.
**Exceptions**|None
<br>

<hr>

Name | Create a PlayList
----|----
**Actor**|Registered User
**Description**|User creates a new personal Playlist.
**Precondition**|Actor is signed-in into a pre-excising User Account.
**Scenario**| Step 1. Actor selects an option to create a new personal Playlist <br> Step 2. Application requests Actor to enter a name for their new Playlist <br> Step 3. Actor enters a name for their new Personal Playlist <br> Step 4. Actor submits the information <br> Step 5. Application ask wheater Actor would like to add songs to their new playlist. <br> Step 6. Actor indicates, if they want to add songs to their new Playlist. <br> Step 7. Application shows Actor that their Playlist was sucessfuly created.
**Result**|User has sucessfuly created a new personal Playlist.
**Exceptions**|4a. System indicates that the entered name is invalid. <br> 4a.1. Returns to Step 2. <br>4b. System indicates that the entered name is already been used for another personal playlist. <br> 4b.1. Returns to Step 2.
**Extensions**| 6a. Actor indicates that they want to add songs to their newly created Playlist<br>     1. Actor <ins>adds songs to their playlist</ins>. <br>       2. Return to step 7. <br>6b Actor indicated that they don't want to add songs to their newly created Playlist<br>       1. Return to step 7. 
<br>

<hr>

Name | Add songs to a playlist
----|----
**Actor**|Registered User
**Description**|An User is adding songs to their personal Playlist.
**Precondition**|User has at least one pre-existing personal Playlist.
**Scenario**| Step 1. Application displays an overview of a Personal Playlist.<br> Step 2. Actor selects an option to add songs to the personal Playlist. <br> Step 3. Application request Actor to Search for a song to be added to the playlist. <br> Step 4. Actor <ins>searches for a song</ins> <br> Step 5. Actor selects the exact song to be added <br> Step 6. Application informs the Actor, that the song was sucessfuly added to the playlist.
**Result**|User sucessfuly added desired songs to their personal playlist
**Exceptions**|None
<br>

<hr>

Name | Remove Songs from Playlist
----|----
**Actor**|Registered User
**Description**|An user is removing songs from one of their personal Playlists.
**Precondition**|The User has at least one pre-excisting Personal Playlist. User should be signed-in into a pre-excisting account
**Scenario**| Step 1. Application displays an overview of a Personal Playlist. <br> Step 2. Actor selects an option to Remove songs from the Playlist <br> Step 3. Application asks Actor to make a selection of which songs should be removed. <br> Step 4. Actor makes a selection of which songs they want to remove. <br> Step 5. Actor submits their choice. <br> Step 6. Application informs Actor, that the selected songs were sucessfuly removed.
**Result**|User has removed a song from their Personal Playlist
**Exceptions**|None
**Extensions**| 4a. Actor selects an option to Cancel the removing. <br>        1.The Use-case ends here.
<br>

<hr>

Name | Rename a Playlist
----|----
**Actor**|Registered User
**Description**|An user changes the name of one of their Personal Playlists.
**Precondition**|The user has at least one pre-excisting Personal Playlist. User should be signed-in into a pre-excisting account
**Scenario**| Step 1. Application shows an overview of User's different Personal Playlists. <br>Step 2. Actor selects options for one of the playlists. <br> Step 3. Application displays the different options for the Playlist. <br> Step 4. Actor selects an option to Rename the Playlist. <br> Step 5. Application requests Actor to enter a new name for the Playlist. <br> Step 6. Actor enters a new name for the Playlist. <br> Step 7. Actor submits their choice of a name. <br> Step 8. Application informs Actor, that the Playlist was renamed sucessfuly.
**Result**|User changed the name of one of their Playlists.
**Exceptions**| 7a. Application informs Actor, that the name entered is invalid <br>        1. Returns to Step 5. <br> 7b. Application informs Actor, that the name is already taken by another Personal Playlist.<br>      1. Return to Step 5.
**Extensions**| 6a. Actor indicates that they want to Cancel the Renaming.<br>      1. Use-case ends here.
<br>
<hr>

Name | Delete Playlist
----|----
**Actor**|Registered User
**Description**|An User wants to delete one of their Personal Playlists.
**Precondition**|The User has at least one pre-excisting Personal Playlist. 
**Scenario**| Step 1. Application displays an overview of User's Personal Playlists <br> Step 2. Actor selects options for one of the playlists <br> Step 3. Applicaiton displays the different options for the Playlist. <br> Step 4. Actor chooses an option to delete the Playlist <br> Step 5. Application requests a confirmation. <br> Step 6. Actor confirms their choice. <br> Step 7. Application informs Actor, that the Playlist was deleted sucessfuly. 
**Result**|User deleted a Personal Playlist  of their choice.
**Exceptions**|None
**Extension**| 6a. Actor selects an option to Cancel the Deletion.<br>      1. Use-case ends here.
<br>

<hr>

Name | View Playlist
----|----
**Actor**|Registered User
**Description**|An User is Viewing one of their Playlists.
**Precondition**|The user has at least one pre-existing Personal Playlist. User should be signed-in into a pre-excisting account
**Scenario**| Step 1. Application displays User's homepage. <br> Step 2. Actor selects an option to view their Personal Playlists. <br> Step 3. Application displays an overview of User's Personal Playlists. <br> Step 4. Actor selects a Playlist of their choice. <br> Step 5. Application displays an overview of the selected Playlist.
**Result**|User sees an overview of their Personal Playlist.
**Exceptions**|None
<br>

<hr>

Name | View personal top-played songs
----|----
**Actor**|Registered User
**Description**|An User sees their personal top-played songs.
**Precondition**|User should be signed-in into a pre-excisting account
**Scenario**| Step 1. Application displays User's Homepage. <br> Step 2. Actor selects an option to view their Personal top-played songs. <br> Step 3. Application shows a Playlist with User's top-played songs.
**Result**|User views their most-played songs.
**Exceptions**|2. System displays a message, that there are not enought songs listened, in order to make the selection. <br>        1. Use-case ends here.
<br>

<hr>

Name | View Country - specific top-played songs
----|----
**Actor**|Registered User
**Description**|An User views the top-played songs in a country of their choice.
**Precondition**|User should be signed-in into a pre-excisting account
**Scenario**| Step 1. Application displays User's Homepage. <br> Step 2. Actor selects an option to View the most-played songs in their country. <hr> Step 3. Application requests Actor to select for which specific country, they would like to see the most-played songs. <hr> Step 4. Actor selects a country and submits their decision. <hr> Step 5. Application displays a Playlist with the top-played songs for the selected country.
**Result**|User sees country-specific top-played songs
**Exceptions**|4. System displays a message, that there is no compilation for this specific country.<br>        1. Use-case ends here.
<br>

<hr>

Name | View number of plays of a song
----|----
**Actor**|Registered User
**Description**|An User views the number of plays of a current song.
**Precondition**|User should be signed-in into a pre-excisting account
**Scenario**| Step 1. Application displays variety of songs. <br> Step 2. Actor selects the options for a specific song. <br> Step 3. Application displays the available options for the song. <br> Step 4. Actor selects the option to View detailed information about the song. <br> Step 5. Application displays additional information, about the specific song, including the Number of plays across users.
**Result**|User sees additional information about a specific song, including the number of plays accross different users.
**Exceptions**|None
<br>
<hr>
<hr>

### Public transport card machine
Through the public transport card machine a traveler can obtain a new anonymous travel card with a certain amount of money, (re)charge an existing anonymous travel card that the traveler inserted or (re)charge their personalized travel card. Additionally, travelers older than 60 owning a personalized card can use the machine to activate a so called 'choice day', which allows the traveler to travel for free during one day as long as they travel outside peak hours. Travelers can activate seven choice days per year.

#### Use cases
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


