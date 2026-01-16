This document and the video do not use AI or contain any AI generated content at any point because I don’t really like it :D
# Overview
Hero Shooter inspired video-game featuring teachers/faculty as playable characters, set on Harvard-Westlake campus.

### Design Video
https://drive.google.com/file/d/1L-IXy8-kMBXeceHR1sNL-zdUtFbFaQgZ/view?usp=drive_link

## 1. Project Details
- Type: Video Game App
- Platform: PC or Mac
- Players: Online Multiplayer
- Auth: Accounts Required

## 2. Purpose
- Provide an entertaining but school friendly online multiplayer game with references to people and locations that Harvard-Westlake students will recognize, making it potentially more appealing.
- Audience: Harvard-Westlake students who enjoy video games.
- Appeal over other online games (In School): No guns or violence, and is part of a school project, which gives students justification for playing in school.
- Appeal out of school: Harvard-Westlake theming can provide fun from getting to play a teacher you like (or joy from fighting against a teacher you don’t).

## 3. Honor Code and Legal Note
- This game will NOT depict firearms, weapons such as knives, swords, bows, or anything like that.
- This game will NOT depict death or killing of any kind, players may “fail” and be sent back to the spawn room, but this is not death, and they return after a few seconds.
- This game does not feature minors, all characters are teachers or faculty and are adults.

# Design
Disclaimer: All design elements are subject to change, if something doesn’t seem right to you, please say something! It won’t hurt feelings, we’re here to make a good product.

If there are brackets around something, (ex: “The floor will be \[red/blue\]”) this indicates that an idea has been narrowed down to a few options but not decided yet. This will be addressed later in the design process.

## Game Start (All Modes)
- Queue into a match with \[10/12\] total players, and get divided evenly into 2 teams. A loading screen showing both teams and their players will be shown, as well as the map and gamemode.
- Select your character from the list of available ones. If a teammate has chosen a character already, it will be unavailable, but you may choose the same character as someone on the opposing side.
- Join into your team’s spawn room, and make your way to the mission area.

## Main Gameplay (Point Capture)
ALWAYS TRUE:  
**Objective Progress will never decrease. This is per team. It starts at 0.**  
**Capture Progress will fluctuate between the two teams. Only one team can have Capture Progress at a time.**  
### Uncaptured
- Point begins uncaptured, once it becomes captured it will not return to the Uncaptured state.
- Contested: At least 1 player from each team on point, Capture Progress pauses where it is.
- Uncontested: 
    - If no players, Capture Progress goes towards neutral. 
    - If only players from 1 team, Capture Progress goes towards them.
- The speed at which Capture Progress goes towards either side is determined by the amount of players on point.
### Captured
- Point becomes captured if Capture Progress is completed for either team. If it is taken by the enemy team, it goes straight to being captured for them, it never returns to Uncaptured state.
- Contested: At least 1 player from each team on point, Objective Progress slows but still continues.
- Uncontested: 
    - If no players, Objective Progress still increases for the team that has captured the point.
    - If only players from team that has captured, progress increases scaled by amount of players
    - If only players from the enemy team, Objective Progress stops and Capture Progress starts going to the enemy team.
### Overtime
- If Objective Progress reaches 99% while being contested, the match goes into overtime, where it will remain at 99% until it stops being contested.
### Win Condition
- Once either team reaches 100% Objective Progress the match ends and the point goes to them.
- Best of 3 overall scoring, with 3 different maps, one for each round. (Randomized order)

## Main Gameplay (Cart)
### Offense
- Goal is to move a cart across the map
- Amount of players on cart when captured increases speed, if no attacking players are on the cart, it doesn’t move
- Once a checkpoint is reached, Offense spawnpoints are moved up, and defense spawnpoints are moved back. Progress cannot go back behind the checkpoint
### Defense
- Goal is to prevent cart from making progress
- Move cart slightly backwards while captured, which scales with the amount of players, but not significantly.
### Win Condition
- Once one round is played, the roles will be swapped and the teams will go again. 
- Whoever has the furthest distance will win, so if the first team only made it 20 meters, the swap means the other team only needs to get to 21 meters for the game to end.
- If both teams make it to the end, another set of rounds will be played.

## Characters
### Passive
- Characters can have different passives, which are any traits that don’t get used or have cooldowns.
- Examples:
    - Movement - Ability to run up walls
    - Resource - Slowly recharging bar of expendable resources that fund other abilities
    - Summon - Create a creature when an enemy falls
### Ability
- Anything that the character has to press a button to activate is an ability, and the number that they have doesn’t have to be the same across the board.
- Abilities have different cooldowns, which should be scaled in accordance with the power of the ability and the ability set as a whole. 
- Certain actions can potentially reduce these cooldowns.
### Ultimate
- Characters have one ultimate ability that charges on its own throughout the battle and is a powerful tool.
- Ult charge is different for each character and builds faster the more the character is doing (healing, damage, shielding, ect…)
- Ultimates shouldn’t be built to win a team fight on their own, but they should be able to swing things in the team’s favor if used optimally.
- Ults can be damage, control, healing/buffs, or some combination of those things, but should generally be in line with the character’s role.
- There should be indicators to allied and enemy teams that a character is ulting (when they do so), and what team they’re on. This is achieved in similar games via voicelines or warning symbols.
### General Design Philosophy
- In general, characters should be built to work with a team, not as a hero that could be thrown in a solo game and do great. (It’s fine if they would do great, but that’s not the goal)
- Characters should have abilities that can assist teammates, particularly if they’re a tank or a support.
- If a character is a dive DPS, they shouldn’t have healing abilities so they still have to play near the healers sometimes, or have to use heal packs. 
- Conversely, support characters should have some form of self healing in order to combat backline diving.
- Characters should have different levels of difficulty to play, so that people of any skill level can still make an impact, but skilled players on harder characters should still be rewarded.

## Art Direction
### Modeling
- Characters will be 3D, and the player will be in first person, so things like hands and powers should be more detailed than legs or feet, which won’t be as visible when playing.
- Maps should try to remain fairly accurate to real life, but can be edited to make a better gameplay experience. Being recognizable is the most important factor.
### UI
- Icons for different abilities that are somewhat recognizable and distinct are important for quickly checking cooldowns during a fight.
- Overall the HUD shouldn’t be too distracting or take up too much of the screen.
- There will be a main menu and log-in system (required) and some way to add friends and invite them to a party.
- Either in a party or alone, the player should be able to queue up while still browsing around.
