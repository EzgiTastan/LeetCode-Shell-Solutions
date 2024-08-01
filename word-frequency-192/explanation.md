## Explanation
In the 192nd question, you should provide the frequency of the words (in the second order) and the words themselves (in the first order) while the number of frequencies is descending.

Meaning that:

- Assume that `words.txt` has the following content:

the day is sunny the the </br>
the sunny is is </br>

- Your script should output the following, (important: sorted by descending frequency):

the 4 </br>
is 3 </br>
sunny 2 </br>
day 1 </br>

My solution is:</br>
cat words.txt | tr -s ' ' '\n' | sort | uniq -c | sort -r | awk '{print $2, $1}'

- Open the `words.txt` file
- In the output, the spaces should be turned into new lines (and each word should have its own line) (`tr -s ' ' '\n' < words.txt`)
- Sorts the words alphabetically (`sort`)
- Count the occurrences of each word (`uniq -c`)
- Sort the counted words in descending numerical order (`sort -nr`)
- Format the output to show the word first and the frequency second (`awk '{print $2, $1}'`)
