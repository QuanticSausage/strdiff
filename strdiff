#!/bin/bash
## program to print differences between two strings in color, and if they differ in length, print the difference in length

if [ $# -ne 2 ];
	then printf "illegal number of arguments! 2 args required\n"
	exit
fi 

STR1=$1
STR2=$2
LEN_STR1=${#STR1}
LEN_STR2=${#STR2}

if [[ ${LEN_STR1} -eq ${LEN_STR2} ]];
	then printf "Length of both strings: ${LEN_STR1}\n"
else
	DIF=$(($LEN_STR1 - $LEN_STR2))
	printf "Length difference: ${DIF}\n"
fi
# Prepare iteration range
if [[ ${DIF} -lt 0 ]];
then  
	END=$LEN_STR1
else
	END=$LEN_STR2
fi
printf "Iteration range ${END}\n"

for ((i=0;i<END;i++)); do
	CHAR1=${STR1:i:1}
	CHAR2=${STR2:i:1}
	if [ "$CHAR1" != "$CHAR2" ];
	then
		printf "\033[0;31m$CHAR1"
	else 
		printf "\033[0;39m$CHAR1"
	fi
done

printf "\n"

for ((i=0;i<END;i++)); do
	CHAR1=${STR1:i:1}
	CHAR2=${STR2:i:1}
	if [ "$CHAR1" != "$CHAR2" ];
	then
		printf "\033[0;31m$CHAR2"
	else 
		printf "\033[0;39m$CHAR2"
	fi
done

printf "\n"

exit
