# ARGQuery
useful Azure ARG queries
# My GitHub Repository

This repository contains various files with data.

## Data Files

- [Queries/GuestConfiguration/1-GetGuestConfigurationAssignments.txt](Queries/GuestConfiguration/1-GetGuestConfigurationAssignments.txt)
- [File 2](file2.csv)
- [File 3](file3.json)


#!/bin/bash

#File: tree-md

tree=$(tree -tf --noreport -I '*~' --charset ascii $1 |
       sed -e 's/| \+/  /g' -e 's/[|`]-\+/ */g' -e 's:\(* \)\(\(.*/\)\([^/]\+\)\):\1[\4](\2):g')

printf "# Project tree\n\n${tree}"
