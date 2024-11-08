# 09 Secret Auction

## Overview

The **Secret Auction** project is a Python program that simulates a blind auction, where participants submit bids anonymously. Developed as part of Day 09 in Dr. Angela Yu's **100 Days of Code: The Complete Python Pro Bootcamp**, this project focuses on using dictionaries to store and retrieve user data.

## Functionality

The program collects each participant's name and bid, saves the data in a dictionary, and determines the highest bid once all participants have entered. To maintain bid secrecy, it clears the output between entries by printing multiple newlines.


## Program Flow
1. **Participant Input**: Users are prompted to enter their name and bid.
2. **Bid Storage**: The name and bid are stored in a dictionary called `bids`.
3. **Check for Additional Bidders**: After each bid, the program asks if there are other bidders. If yes, it clears the output and prompts the next bidder. If no, it proceeds to determine the winner.
4. **Determine Winner**: The `find_highest_bidder` function scans through the dictionary to find and display the highest bid.

## Example Code Snippet
The following code snippet shows how bids are evaluated to find the winner:
```python
def find_highest_bidder(bidding_dictionary):
    highest_bid = 0
    for bidder in bidding_dictionary:
        bid_amount = bidding_dictionary[bidder]
        if bid_amount > highest_bid:
            highest_bid = bid_amount
            winner = bidder
    print(f"The winner is {winner} with a bid ${highest_bid}.")
```

## Sample Output
```
What is your name?: Alice
What is your bid?: $200
Are there any other bidders? Type 'yes' or 'no':
yes

... (other entries)

The winner is Alice with a bid of $200.
```
<!-- 
## License
This project is developed as part of Dr. Angela Yu's **100 Days of Code: The Complete Python Pro Bootcamp** and is intended for educational purposes.
 -->

---
<section align="center">
  <code>coderBri © 2024</code>
</section>