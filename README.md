# Test1

part1

 * mkdir Submissions create directory in my directory
 
•	Go to /home/cumoja1/3320/test1
•	Then use “find data.tar”
find data.tar

•	I found “data.tar” file in the directory now copy file into my directory
•	cp command will help me to copy and put it into my directory
cp /home/cumoja1/3320/test1/data.tar /home/clee195/Submissions/Test1/data.tar

•	Use tar command to extract data. tar file
tar -xvf data.tar

•	Commend grep -ic “computer science” … runs search computer science in files and counting then print
grep -ic "computer science" Badges.xml Tags.xml Votes.xml Comments.xml PostHistory.xml Posts.xml Users.xml

•	grep -n … > computer-science does copy the result and paste into the computer-science file
grep -in "computer science" Badges.xml Tags.xml Votes.xml Comments.xml PostHistory.xml Posts.xml Users.xml
 > computer-science
 
•	‘data|structures’ : searching words data or structures
•	Grep -Ec ‘data|structes’ … : shows how many times it used in the files
grep -Ec 'data|structures' Badges.xml Tags.xml Votes.xml Comments.xml PostHistory.xml Posts.xml Users.xml

•	touch : create file
touch data-structures

•	grep -n … > … : copy the data and replace into the data-structure file
grep -n 'data|structures' Badges.xml Tags.xml Votes.xml Comments.xml PostHistory.xml Posts.xml Users.xml
 > data-structures

•	‘http?://[^ ]+’ : find the URL link
•	grep -c ‘http?://[^ ]+’ … : find URL Link and print out
grep -c 'http?://[^]+' Badges.xml Tags.xml Votes.xml Comments.xml PostHistory.xml Posts.xml Users.xml

•	touch : create file command
•	grep … > websites : copy the data and paste in the file named websites
touch websites
grep -n 'http?://[^]+' Badges.xml Tags.xml Votes.xml Comments.xml PostHistory.xml Posts.xml Users.xml > websites

•	Using cat command combine files into “1.part”
•	cat computer-science data-structures websites > 1.part
cat computer-science data-structures websites > 1.part


Part2
•	wget : command for download file from url directly
wget https://data.ct.gov/api/views/rybz-nyjw/rows.csv

•	cat rows.csv allows us to read the file inside, awk -F ',' rows.csv allows make it format by comma
cat rows.csv
awk -F '.' rows.csv

•	NF==5,6: erase column if it is empty
awk 'NF == 5,6' rows.csv > 2.parse

•	Awk ‘{print $4, $5, $6}’ : shows in column
•	Awk ‘{print $4, $5, $6}’ > 2.asr copy the columns 4-6 but in my file it contains some other contents
•	So I use grep: grep ‘\|Male\|Female’ 2.asr
•	It only contains age, sex, and race
awk '{print $4, $5,$6}'
awk '{print $4, $5,$6}' > 2.asr
grep '\|Male\|Female' 2.asr

•	Grep -c: counts the certain word in line in file
grep -c "Male" 2.asr
grep -c "Female 2.asr

•	Awk ‘{total += $1} END {print total/3774}’ ageM.ageF
•	This commend does calculate average of man/female
i.	ageM,ageF is file only contains age
  awk '{total += $1} END {print total 3774}' ageM
  awk '{total += $1} END {print total 3774}' ageF

•	Awk ‘{A[$3]++} END {for(I in A) print I, A[i]}’ 2.asr count words that duplicates
 awk '{A[$3]++} END{for(i in A) print i,A[i]}' 2.asr
 
•	Grep two words in one line command is: grep “White” rows.csv | grep -c “Male”
grep "White" rows.csv | grep -c "Male"
grep "White" rows.csv | grep -c "Female"
grep "Black" rows.csv | grep -c "Male"
grep "Black" rows.csv | grep -c "Female" 
 
•	Wmlist,wflist,bmlist,bflist contains only age of each races
•	Awk ‘{total +=$1} END {print total/NR}’ file shows average of number
awk ‘{total +=$1} END {print total/3374}’ wmlist
awk ‘{total +=$1} END {print total/1187}’ wflist
awk ‘{total +=$1} END {print total/342}’ bmlist
awk ‘{total +=$1} END {print total/117}’ bflist

•	Awk ‘BEGIN {a=1000} {if($1<0+a) a = $1} END {print a}’ file shows min
awk 'BEGIN{a = 1000} {if($1<0+a) a = $1} END {print a}’ wmlist
awk 'BEGIN{a = 1000} {if($1<0+a) a = $1} END {print a}’ wflist
awk 'BEGIN{a = 1000} {if($1<0+a) a = $1} END {print a}’ bmlist
awk 'BEGIN{a = 1000} {if($1<0+a) a = $1} END {print a}’ bflist

•	Awk ‘BEGIN {a=0} {if($1>0+a) a = $1} END {print a}’ file shows max
awk ‘BEGIN {a=0} {if($1>0+a) a = $1} END {print a}’ wmlist
awk ‘BEGIN {a=0} {if($1>0+a) a = $1} END {print a}’ wflist
awk ‘BEGIN {a=0} {if($1>0+a) a = $1} END {print a}’ bmlist
awk ‘BEGIN {a=0} {if($1>0+a) a = $1} END {print a}’ bflist

github submit
git init
git add .
git -m "first commit"
git remote add origin https://github.com/clee9604/Test1.git
git remote set-url origin https://github.com/clee9604/Test1.git
git push -u origin master --force
