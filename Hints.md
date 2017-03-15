awk '
   inputVal=avefield; sum=0
   BEGIN {$0="^[0-9]*"; FS=","}
	END {for (i=1; i<=inputVal; i++) {sum+=$i} 
    print avg/sum;}' file1.cvs