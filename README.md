# mudlet_fadescript
Mudlet Fade Script

To install: Go to "Triggers" or "Aliases" and select "Import", then import these triggers and aliases.

Note this is designed for use with Adael's WoTMUD Mudlet system: https://github.com/weisluke/WoTMUD

To use:
* Be a rank 3 fade (see notes on modifying for other ranks below)
* Type SENSEFROM <zone>, where supported zones are TKD, GORTHEL and WBFADE
* The triggers will turn on while sensing, and disable when done, so they don't lag mudlet
* The script will parse all the codes that are output, and store the captured ones as fade codes (note, unlike the similar zmud script, it doesn't store ALL codes, since I find the paradox of choice overwhelming)
* You can do VIEWFADECODES to see the list of codes and name mappings
* You can now do FADETO <place> to fade to that code, e.g., FADETO TKD or FADETO RK
* The codes will automatically be cleared at the month change, to prevent misfading (you will have to manually cancel any in-progress fade or else you'll end up misfading -- the script does not do that for you)

To modify for ranks other than 3:
* The codes are designed for a rank 3 fade, but can be updated for other ranks. (ranks 1 and 2 I've already mapped out)
*  Use this spreadsheet that maps the order of codes on sense: https://docs.google.com/spreadsheets/d/1Vvo98IPwUU0RymqbWwZ2BI71wfUaB4VAjzM9dSondTg/edit#gid=119106010
*  Select the appropriate rank tab, and in the fade trigger, update the if/then iteration that maps sequential numbers in sense to the codes you want to store
