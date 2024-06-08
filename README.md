# rsgb-data

Automatically snapshotting the data returned from https://api-beta.rsgb.online/all/systems

The process runs it through `jq` to format it consistently before committing it [here](https://github.com/Online-Amateur-Radio-Club-M0OUK/rsgb-data/blob/main/data/all-systems.json) ([raw](https://raw.githubusercontent.com/Online-Amateur-Radio-Club-M0OUK/rsgb-data/main/data/all-systems.json)).

Here’s a brief overview of the API endpoints and their functions:

/all: Returns all public listings when any string is passed as an argument.
/aprs: Given a callsign, it returns the APRS passcode.
/band: Returns listings for a specific band when the band name is provided.
/callsign: Returns listings associated with a specific callsign.
/keeper: Returns listings for a keeper given the keeper’s callsign.
/locator: Returns listings for a locator square when the locator string is provided.
Additionally, there are mode flags that can be appended with specified access codes to indicate the mode of communication:

A: Analogue
D: D-STAR
E: Tetra
M: DMR
F: Fusion
P: P25
7: M17
N: NXDN
PX: Packet Mailbox
X: Regenerative Node
For example, for DMR with color code 1, you would append ["M:1"] to the mode flag.
