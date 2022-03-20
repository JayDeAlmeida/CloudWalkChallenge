Log parser

Create a project to parse the Quake log file.

The log file was generated by a Quake 3 Arena server, including a great deal of information of every match.

The project should implement the following functionalities:

Read the log file
Group the game data of each match
Collect kill data
Example
21:42 Kill: 1022 2 22: <world> killed Isgalamido by MOD_TRIGGER_HURT
The player "Isgalamido" died because he was wounded and fell from a height enough to kill him.

2:22 Kill: 3 2 10: Isgalamido killed Dono da Bola by MOD_RAILGUN
The player "Isgalamido" killed the player "Dono da Bola" using the Railgun weapon.

Example of grouped information for each match:

"game_1": {
"total_kills": 45,
"players": ["Dono da bola", "Isgalamido", "Zeh"],
"kills": {
  "Dono da bola": 5,
  "Isgalamido": 18,
  "Zeh": 20
  }
}
Additional notes:

When <world> kill a player, that player loses -1 kill score.
Since <world> is not a player, it should not appear in the list of players or in the dictionary of kills.
The counter total_kills includes player and world deaths.
  
  Create a script that prints a report (grouped information) for each match and a player ranking.
  
  Generate a report of deaths grouped by death cause for each match.
