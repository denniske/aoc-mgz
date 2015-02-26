# mgz

AoC MGZ parsing in Python 2.x.

### Usage
 - Complete file:
   - mgz.parse(file)
 - Incomplete file (spec):
   - header.parse(file)
   - Loop: body.command.parse(file)

### Caveats
 - Parses only portions useful for multiplayer recorded game analysis
 - UserPatch 1.4 only

### Dependencies
 - construct: https://github.com/construct/construct

### Contribution
 - Pull requests & patches welcome

### Resources
 - aoc-mgx-format: https://github.com/stefan-kolb/aoc-mgx-format
 - node-aoe-rec: https://github.com/goto-bus-stop/node-aoe-rec
 - recanalyst: http://sourceforge.net/p/recanalyst/

### Output

General format of the file, noting interesting parts.
- Header
  - Version
  - AI
  - Record properties
    - Speed
    - Number of players
    - View of
  - Map
    - Size
    - Tiles
  - State
    - Start time
    - Players[]
      - Name
      - Diplomacy
      - Civilization
      - Color
      - Camera
      - Objects[]
        - Type
        - ID
        - Position
  - Achievements[]
  - Scenario
    - Instructions
    - Players[]
    - Victory condition
    - Map type
    - Difficulty
    - Triggers
  - Lobby
    - Teams
    - Reveal map
    - Population limit
    - Game type
    - Lock diplomacy
    - Pre-game chat
- Body
  - Commands[]
     - Sync, Message, or Action
