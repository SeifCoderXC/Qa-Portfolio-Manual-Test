# Exploratory charters

Timebox 45 minutes each. Stop when the clock stops. Notes go under the charter, not into a new document.

## CH-01 — New Game and first turn

Explore New Game options and the first-turn HUD to find start failures, disabled Start with no reason, and map-gen hangs.

Areas: civilization list, difficulty, map type/size, opponents, Start, first-turn selection, Next Turn.

Wrong looks like: spinner never ends, Start does nothing with every field filled, first turn with zero units and no settler, UI widgets overlapping so a control cannot be clicked.

Setup: mods off, tiny map.

Stop reason: _  
Bugs: _  
Questions: _

## CH-02 — City and production

Explore the city screen after founding to find queue mistakes and dual-button crashes.

Areas: found city, rename if offered, production list, queue reorder if present, buy/hurry if present, citizen assignment if present.

Wrong looks like: production selected but city still idle, queue item vanishes, crash when two city-screen arrows are used together (see BUG-003).

Setup: game from CH-01 or TC-006.

Stop reason: _  
Bugs: _  
Questions: _

## CH-03 — Persist and recover

Explore save, load, continue, and crash files.

Areas: Save dialog, save list, Load, Continue, `SaveFiles/`, `lasterror.txt` if present, autosave if Options enabled it.

Wrong looks like: name saved but missing from list, load of the same turn on a different map, continue starts New Game, process death with no lasterror.

Setup: named save from TC-018.

Stop reason: _  
Bugs: _  
Questions: _
