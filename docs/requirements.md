# Requirements (player-facing)

Derived from the public desktop product. IDs are local to this pack.

| ID | Name | Statement | Area |
|---|---|---|---|
| REQ-01 | Launch | Game window opens from `java -jar` / desktop launcher and shows the main menu. | Stability |
| REQ-02 | New game | Player can choose civilization, difficulty, map type/size, opponent count, then start a single-player game. | New Game |
| REQ-03 | First turn | After start, the map is visible, at least one unit or settler is selectable, and Next Turn is available. | New Game |
| REQ-04 | Found city | Settler can found a city on a legal tile. City screen opens. | Cities |
| REQ-05 | Production | City can queue a unit or building. Queue shows the selected item. | Cities |
| REQ-06 | Tech | Tech picker opens, a researchable tech can be selected, and the selection persists on Next Turn. | Tech |
| REQ-07 | Move unit | A unit with movement left can move to an adjacent legal tile. | Units |
| REQ-08 | Combat | A military unit can attack an adjacent hostile unit or city when rules allow. Result changes HP or removes a unit. | Units |
| REQ-09 | Save | Player can save to a named slot. File appears in the save list. | Persist |
| REQ-10 | Load | Load of that save restores turn, map, and city/unit state. | Persist |
| REQ-11 | Continue | Continue / last game returns to the same match after a clean quit. | Persist |
| REQ-12 | Options persist | A display or autosave option change is still applied after restart. | Options |
| REQ-13 | Window | Resizing the window keeps the map and buttons usable. No permanent black panel. | Usability |
| REQ-14 | Civilopedia | Civilopedia opens from the menu and shows an entry without freezing the UI. | Stability |
| REQ-15 | No-mod isolation | With mods disabled, New Game does not pull a custom ruleset. | New Game |
