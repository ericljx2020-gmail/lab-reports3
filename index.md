# Lab Report 3(Week 5)

## `grep -v`
`grep` was used to check if a specific string is in the target file or not. If it is in the file, it will output the specific line it is located. 
**However when you add a -v to the end, it will output all the lines that does not contain the string given.**

*Examples*
1. Use grep -v to find all the file that doesn't contain "China" in the file name
```
find written_2/ -name "*China*.txt" > find_CN.txt                  --Used to find all the txt files that has China in the name and write it into a file

find written_2/ -name "*.txt" > alltx.txt                          --Used to find all the txt files in the written_2 directory and write it into a file

grep -v "China" alltx.txt > noCN.txt                               --Used to find files that doesn't have China in itusing grep -v.

grep "China" noCN.txt                                              --Trying to find China in noCN.txtm and there is no "China"
output: N/A

grep "China" alltx.txt                                             --Proving that there are txt files in the directory that contain China in the file name.
output:
written_2/travel_guides/berlitz2/China-History.txt
written_2/travel_guides/berlitz2/China-WhatToDo.txt
written_2/travel_guides/berlitz2/China-WhereToGo.txt
```

2. Use grep -v to find lines in *Bahamas-History* that doesn't contain "Lucayans"
```
grep -v "Lucayans" written_2/travel_guides/berlitz2/Bahamas-History.txt > noLucas.txt.        --noLucas is a file contains all the line of Bahamas-History.txt, except for those containing Lucayans

grep "Lucayans" written_2/travel_guides/berlitz2/Bahamas-History.txt                          --this is a proof that Bahamas-History.txt contains Lucayans
output:
Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```
