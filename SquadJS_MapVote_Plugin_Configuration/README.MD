[H1] Galactic Contention SquadJS configuration snippet for mapvote plugin snippet [H1]

The MapVote plugin for squad js based on the original version https://github.com/maskedmonkyman/squad-js-map-vote
Commands
User Commands

    !vote help - sends possbile commands to a player in the from of a warning
    !vote choices - sends choices to player in the from of a warning
    !vote results - sends player the results in a warning

Admin Commands

    !vote start - Starts a vote with 6 layers, random modes
    !vote cancel - Cancels current round of voting
    !vote cancelauto - Cancel scheduled automatic start of vote
    !vote end - Gently ends the current vote and announces the winner layer
    !vote restart - Restarts voting with 6 random maps and modes
    !vote broadcast - Broadcasts current voting results - happens every 7m automatically
    !vote endmatch - Ends the current match

Vote by modes

    !vote start *_raas - Starts a vote with 6 layers, all RAAS
    !vote start *_aas - Starts a vote with 6 layers, all AAS
    !vote start *_inv - Starts a vote with 6 layers, all INV

Vote by faction

    !vote start f:rus - Starts a vote with 6 layers, all with RUS faction
    !vote start f:aus - Starts a vote with 6 layers, all with AUS faction
    !vote start f:mea f:caf f:usa - Starts a vote with 3 layers, 1 with MEA faction, 1 with CAF faction and 1 with USA faction

Vote by map

    !vote start yeh gor lash gor albas - Starts a vote with X maps, random modes

Vote by map + mode, mixed

    !vote start yeh_raas gor_raas lash_inv gor albas_inv - Starts a vote with X maps, X modes

DBLog

Configure the DBLog SquadJS plugin, nothing more is required.
