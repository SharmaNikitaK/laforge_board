# LaForge_Board

## Project Goals
The goal of this project is to improve accessibility of tabletop RPGs for the visually impared. The mechanism is a matrix of individually addressable RGB illuminated buttons. The button matrix will take the role of a standard battle map. Button color may be set by players pressing a button to move their token or by a terminal operator calling functions to change buttons. 

<details><Summary>LaForge Board layout</summary>
 <p>
  <img src="https://raw.githubusercontent.com/SharmaNikitaK/laforge_board/master/laforge_general_layout.png" alt="LaForge Board Layout" href="https://raw.githubusercontent.com/SharmaNikitaK/laforge_board/master/laforge_general_layout.png"/>
 </p>
</details>

## Physical Design Notes
* The board must have a toggle switch to control whether buttons change color based on touch. This is to allow for physical interaction with the buttons without changing the map.
* Each player must have a button they can press to set the board to the proper mode for that player to move their token. The interaction would be the following: the player presses their button then presses on the board where they intend to move to. The board will change their old position light to whatever existed on the map layer, then will light their new position with the player's color.
* The board must provide audio and tactile feedback E.G. Key switches provide audio feedback when buttons are pushed and an embossed letter and number grid is provided along the length and width of the board.
* Visual accommodations should include High Contrast, enlarged buttons and symbols, reduced flicker rates, etc.
## Software Design Notes
* There must be a map layer and a token layer held in memory to accomodate tokens moving.
* The save files should be CSV formatted hexidecimal color codes.
* There must be a way for the operator to set board colors via the console.
  * At some point, we will create a GUI for the operator so they can more easily design encounters.
* There must be a way for the operator to set multiple button's colors simultaniously.
* There must be a way for the operator to set shapes to a color. For example, they could create a rectangle from `B-3` to `O-12` to color `#c4de91`.
  * At some point, we will implement the ability to place patterns onto the board. This would accomodate placing indicators for auras such as *Bardic Performance*.

## Tasks
1. Design an API for addressal of buttons, import/export of configurations for different maps and encounters
2. Source light panel buttons to allow for creation of physical board
3. Design electronics for board
