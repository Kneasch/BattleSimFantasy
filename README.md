# BattleSimFantasy Documentation
##### Last Updated - 3.14.18

### Founders

#### Nick Fennell - Co-Founder
> Sole Developer

#### Brennan Cross - Co-Founder
> Creative Director

### Gameplay Mechanics

#### Step 1: Initial Request

> When setting up a match, UserA will send UserB a request for a match. When sending the request, UserA will select his/her units from his/her collection. To begin a match, both players are required to select five units to take into the arena. After the initial request is sent, UserA now waits on UserB to accept the request.

#### Step 2: Accepting the Request

> When UserB has accepted the request from UserA, UserB will now select his/her units to take into the arena. While UserB is doing this, UserA will be in a separate phase. UserA has already selected his/her units, so they move into the "Set Up" phase. In this phase, UserA will drag his/her units from their hand onto the `GameBoard`. This allows users to place his/her units in any order they would like. The order does not matter in game, but it gives the user the option to arrange his/her units anyway they like. `Note: The "Set Up" phase is likely to be removed at a later time.`

#### Step 3: Beginning the Match

> Once both users are done with the "Set Up" phase, the backend will randomly pick who goes first. Once decided, both users are allowed to view the `GameBoard`. Even if it is not the user's turn, he/she can still view the `GameBoard`. If it is the user's turn, they will be present with dropdown menus and a few sets of buttons. If it is not the user's turn, the user will not have these options, and the page will automatically refresh every 10 seconds.

#### Step 4: Attacking / Defending

> When it is the user's turn, he/she has a couple of options. For starters, each of the user's alive units much perform an action. They can either attack or defend. If attacking, the unit will lock in the attack on whichever enemy unit is selected in the dropdown menu. If defending, the unit will lock in "Healing..." in the damage dropdown. Defending allows units to regain a small amount of health instead of attacking. There is no cap on unit health, and it can increase infinitely. Please note that the UI/UX will have a severe overhaul later, and will be much more fluid in the future. Once an action has been performed on each unit, the user is prompted with a button to submit their move. This will take the user to a new page that will have short animations that go through each unit action. If the user would like, they can view each attack on this page. Otherwise, there is a button at the top right of this page that will return the user to the `GameBoard`.

#### Step 5: The Game Loop

> Step 4 (Attacking / Defending) will repeat for each user until a winner has been decided. Each time a submission is made, the database is updated with new information and it will switch to the opposing user's turn. After a winner has been decided, the winner will submit the match, and XP and Coin will be given to both users. The winner will always receive 150 XP and 150 Coin for winning. The loser will earn 25 XP and 25 Coin based on how many enemy units they destroyed. For example, if the winner has 3 units left, the loser will receive 50 XP and 50 Coin. `Note: Coin and XP are earned at the same rate, but are different. If you spend Coin, you are not spending XP.`
