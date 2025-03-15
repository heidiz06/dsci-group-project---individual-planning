# dsci-group-project---individual-planning

Author: Heidi


1. Data Description

player.csv = #1
sessions.csv = #2


summary statistics
#1: - 5 unique categories, with "Amateur" being the most common.
    - more than half of the users are subscribed
    - play hours from a minimum of 0 hours to a maximum of 223.1 hours
    - average age of the players: around 20 yrs   
#2: - has full data for hashedEmail and start_time, but end_time and original_end_time are missing in 2 entries.
    - the start_time and end_time columns appear to be in DD/MM/YYYY HH:MM format but are stored as strings.



number of variables
#1: 7
#2: 5


name of variables:
#1: - experience
    - subscribe
    - hashedEmail
    - played_hour
    - name
    - gender
    - Age    
#2: - hashedEmail
    - start_time
    - end_time
    - original_start_time
    - original_end_time
    
type of variables:
#1: factor and numeric
#2: character and numeric


what the variable means:
#1: - experience = the player's skill level
    - subscribe = whether the player has a subscription
    - hashedEmail = a hidden version of the player's email
    - name = the player's name
    - gender = the player's gender
    - played_hour = the number of hours the player has spent playing
    - age = the player's age
#2: - hashedEmail = a hidden version of the player's email --> user ID
    - start_time = time when the player's session started
    - end_time = time when the player's session ended
    - original_start_time = The same as start_time, but stored as a number
    - original_end_time = The same as end_time, but stored as a number


issues seen in the data:
#1: - the variable "age" has two missing values
    - the variable "gender" has a few values with typos and misspellings
    - the variable "played_hour" could have an outlies (223.1 hours)
    - the variable "experience" has some values that are too vague
    - there is no explanation for how the data was being tracked, which might make others question the reliability of certain data such as the numerical variables, age, and played_hour   
#2: - can only access the data on ipad; can't see the values when accessing on laptop
    - The time format does not specify which timezone the timestamps are in, which could cause confusion
    - end_time and original_end_time have missing values, meaning some sessions don’t have an end time recorded
    - some sessions might have an end_time that is earlier than start_time, which would be incorrect
    - start_time and original_start_time store the same information in different formats, which may not be necessary


potential issues related to things that cannot be directly seen:
#1: - Some users have 0 played hours but are in the dataset, likely due to a tracking issue
#2: - The dataset does not specify which timezone the timestamps are in
    - Since emails are hashed, we cannot check if multiple hashed emails belong to the same person
    - If the data collection method only captures certain types of users, the dataset may not represent all users


how the data were collected:
#1: in-game tracking of playtime.
#2: using event logging from the game's app or website


2. Questions
#1: Can experience predict the age of the players in "players.csv"?
#2: Can session start time predict the session end time in "sessions.csv"?
