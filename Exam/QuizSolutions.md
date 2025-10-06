1. grep regex for time range (1:20 PM to 1:30 PM) in access.log

Question:
What grep command matches log lines whose timestamp is between 1:20 PM and 1:30 PM?
What does it capture, and why?

Solution:

grep -cE '\[[^]]*:13:(2[0-9]):[0-9]+' access.log


Explanation:

\[ matches the opening [ before timestamp

[^]]* consumes everything up to time part

:13: matches hour = 13 (1 PM)

(2[0-9]) matches minutes 20 through 29

:[0-9]+ matches the seconds part

-cE + -E for extended regex, -c counts lines matched




2. grep — count IPs starting with 192

Question:
How many logs use a client IP that starts with 192? What is a safe regex for that?

Solution:

grep -cE '^192\.[0-9]+\.[0-9]+\.[0-9]+' access.log


Explanation:

^192\. ensures the line begins with “192.”

Then \.[0-9]+ for the other octets

-cE counts matches using extended regex



3. sed to convert HTML tags to Markdown

Question:
Given sedfile.html, write sed commands (with -i) to transform it to Markdown:

Remove closing tags </...>

Convert <li> to -

Convert <h1> to # and <h2> to ##

Remove <ul>, </ul>, <html>

Replace “Batches” with “Matches”

Solution:

sed -i 's|</[^>]*>||g' sedfile.md
sed -i 's|^[[:space:]]*<li>|- |g' sedfile.md
sed -i 's|<h1>|# |g' sedfile.md
sed -i 's|<h2>|## |g' sedfile.md
sed -i 's|<ul>||g; s|</ul>||g; s|<html>||g' sedfile.md
sed -i 's|Batches|Matches|g' sedfile.md


Explanation:

s|</[^>]*>||g removes any closing tag

^[[:space:]]*<li>|- matches <li> possibly preceded by spaces

The |...|...|g syntax uses | as delimiter instead of / (for readability)

The combined sed -i '...; ...; ...' does multiple replacements





4. awk queries on sales.txt

Question:
Write awk commands to:

Print lines for sales made in February 2024

Print product names with unit price ≥ 100

Print product and quantity for items including “TV” in name

Sum total revenue for category “Kitchen”

Replace all “Sofa” by “Couch” and write to updated-sales.txt

Solution:

awk '/2024-02/' sales.txt
awk '$5 >= 100 {print $2}' sales.txt
awk '/TV/ {print $2, $4}' sales.txt
awk '/Kitchen/ {sum += $6} END {print sum}' sales.txt
awk '{gsub(/Sofa/, "Couch"); print}' sales.txt > updated-sales.txt


Explanation:

/2024-02/ matches date strings in that month

$5 >= 100 {print $2} prints the product field when unit price ≥ 100

/TV/ {print $2, $4} prints name + quantity for “TV” items

Accumulate with sum += $6 for revenue and print at END

gsub(/Sofa/, "Couch") replaces all Sofa with Couch in each record



5. Git & branching — push rejection scenario

Question:
You try to git push origin main but get:

error: failed to push some refs ... fetch first
hint: Updates were rejected because the remote contains work that you do not have locally.


What do you do to fix it?

Solution:

First, commit or stash your local changes:

git add -A
git commit -m "WIP before pulling"


Then pull with rebase:

git pull origin main --rebase


Then push:

git push origin main


Alternatively, if you don’t care about remote changes:

git push --force


(But only use that if you're certain.)

Or discard your local changes:

git restore .
git pull origin main --rebase
git push origin main
