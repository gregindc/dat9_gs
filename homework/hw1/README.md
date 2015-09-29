# Homework 1 description

Using chipotle.tsv in the data subdirectory:
Look at the head and the tail, and think for a minute about how the data is structured. What do you think each column means? What do you think each row means? Tell me! (If you're unsure, look at more of the file contents.)
How many orders do there appear to be?
How many lines are in the file?
Which burrito is more popular, steak or chicken?
Do chicken burritos more often have black beans or pinto beans?
Count the number of occurrences of the word 'dictionary' (regardless of case) across all files in the DAT9 repo.
Optional: Use the the command line to discover something "interesting" about the Chipotle data. The advanced commands may be helpful to you!

# Homework 1 Answers
**Question:** Look at the head and the tail, and think for a minute about how the data is structured. What do you think each column means? What do you think each row means? Tell me! (If you're unsure, look at more of the file contents.)

**Answer:** The data appears to be a set of order data, tab delimited, for Chipotle that includes an order id, quantity, product name, toppings/options, then item price. It appears to include both drinks and food.

**Question:** How many orders do there appear to be? 
**Answer:** There appear to be 1834 orders, according to order id.

**Question:** How many lines are in the file?
**Answer:** Using the command wc, there are 4623 lines. 

**Question:** Which burrito is more popular, steak or chicken?
**Answer:** Using `cut -f 2-3 chipotle.tsv | sort | uniq -c| sort | grep Burrito` to determine the count, I get 591 Chicken Burritos and 386 Steak.

**Question:** Do chicken burritos more often have black beans or pinto beans?
**Answer:** Using `cut -f 2-5 chipotle.tsv | grep 'Chicken\sBurrito' | grep 'Pinto\sBeans' -c` and `cut -f 2-5 chipotle.tsv | grep 'Chicken\sBurrito' | grep 'Black\sBeans' -c` shows that Black Beans occur more frequently than Pinto Beans.

**Question:** Count the number of occurrences of the word 'dictionary' (regardless of case) across all files in the DAT9 repo.
**Answer:** Using `grep -R -c -i dictionary *`, I see two instances of the word in the entire repo.





