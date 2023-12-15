# Analysis & Design: Assignment 1 
## Music Streaming App
### Solution by Mino Karadzhov


### Use cases
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


### Use case descriptions

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

### Use-case Diagram
![Use-case Diagram](https://github.com/FontysVenlo/aade-2020-assignments-aade-2020-g04/blob/master/assignment1/Music_app_use_case_diagram_Mino_Karadzhov.svg)
<br>

### Domain Model
![Domain Model](https://github.com/FontysVenlo/aade-2020-assignments-aade-2020-g04/blob/master/assignment1/Domain_Model_Music_App_Mino_Karadzhov.svg) 


