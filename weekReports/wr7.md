---
Name: Seven Gunthrope
course: cis 106
semester: fall 23
---

# The cat command
This command is used for displaying content inside of a file 
the formula it  uses is cat + option + files to display and two examples of it are:
cat games.txt displays what is the content inside of games.txt
cat -n chips.pdf displays the content of chips.pdf with line numbers

## The tac command
This command is used for displaying files in reverse order
the formula it uses is tac+ option+ files to display examples are:
tac list.txt prints the content of list in reverse order

## the head command
this command is used for displaying top lines of a file
the formula is head+option+files and examples are:
head games.py displays the first 10 lines of games
head -1 chips.py displays the first line of chips

## The tail command
the tail command is used to display the last number of lines in a file
the formula it uses is tail+option+file and examples are:
tail games.csv prints the last 10 lines of games.csv
tail -3 games.csv prints the last 3 lines of games.csv

## The cut command
the cut command is used to extract a specfic section of each lin of the file and display it
the formula it uses is cut+option+file and examples are:
cut -d ':' -f1 /etc/passwd cuts the first field and uses : as the delimiter 
cut -d ':' -f1 --output-delimited="-" /etc/passwd prints all the users and changes the output delimited to -

## The Paste command
the paste command is used for joining files horizontally in columns
the formula is paste + option + file and the examples are:
paste games.csv chips.txt merges both files
paste -d "?" games.csv chips txt merges both files and changes to delimiter to ?

## The Sort command
The sort command is used for sorting files
the formula it uses is sort + option + file examples are:
sort game.csv sorts the file contents in alphabetical order
sort -r games.csv sorts the file contents in reverse order

## The wc command
the wc command is used for printing the number of lines
the formula used is wc+option+files and examples are:
wc -w games.csv prints the number of words in the file
wc -m games.csv prints the number of characters in the file

## The tr command
the tr command is used for translating or deleting characters from standard output
the formula standard | tr + option + set + set and examples are:
cat chips.txt | tr '.' ';' changes periods inside of a file with semi colons
cat games.csv | tr -s "[:lower:]" "," translates each repeated lower case letter inside games.csv with commas

## The diff command
the diff command compares files and displays the differences
the formula diff + option+ file1+file2 and examples are:
diff shoes.txt games.csv shows the differences between shoes and games contents
diff -q shoes.txt cereal.txt report only when files differ

## the grep command
grep is used to search text in a given file
the formula used is grep + option + search criteria + files and examples are:
grep 'shoes' ~/Downloads/nike.txt searches for the word shoes inside of nike
grep -i 'word' ~/cis106 searches for the word regardless of case sensitivity

## The awk command
awk is a scripting language used for processing and displaying text adn can work with a text file or from standard output
the formula for the awk command is awk + option + awk command + file +file to save(depends) and Examples are:
awk '(print $3)' vibes.txt print the third column of every line of vibes
awk -F: '{print $7}' /etc/passwd prints the seventh field of the field
awk 'NR > 5 { print }' /etc/passwd starting printing a file after the 4th line
awk '{print length($0)}' /etc/passwd prints the length of a record
awk -F: '{print toupper($1)}' /etc/passwd prints users in your computer in the uppercase

## The sed command
Sed is a stream editore that performs operations on files and standard output 
the formula is sed options + sed script + file and examples are:
sed 's/onions/peppers' grocerystock.csv changes onions for peppers inside of grocerystock
sed '1d' store.txt removes the first line in store
sed 'G;G'  concert.txt places two blank lines after each line in concert
sed 's/sun/clouds/g' earth.txt replaces all occurences of sun with clouds
sed '/abc/d' alphabet.txt deletes the line that matches the pattern