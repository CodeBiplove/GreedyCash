# CoinChanger

# Cash
![Coin Pic](GreedyCash\Images\coins.jpg)

## Problem to Solve
Suppose you work at a store and a customer gives you $1.00 (100 cents) for candy that costs $0.50 (50 cents). You’ll need to pay them their “change,” the amount leftover after paying for the cost of the candy. When making change, odds are you want to minimize the number of coins you’re dispensing for each customer, lest you run out (or annoy the customer!). 

Implement a program in C that prints the minimum number of coins needed to make the given amount of change, in cents. The program should take in the amount owed as input and output the minimum number of coins, using U.S. coins: quarters (25¢), dimes (10¢), nickels (5¢), and pennies (1¢). 

---

## Description
This C program solves the CS50 Cash Problem by calculating the minimum number of coins required to make change for a given amount in cents, using a greedy algorithm. The program efficiently handles coins of 25¢, 10¢, 5¢, and 1¢ to minimize the number of coins given as change.

## Greedy Algorithms
Fortunately, computer science has given cashiers everywhere ways to minimize the number of coins due: greedy algorithms.

According to the National Institute of Standards and Technology (NIST), a greedy algorithm is one “that always takes the best immediate, or local, solution while finding an answer. Greedy algorithms find the overall, or globally, optimal solution for some optimization problems, but may find less-than-optimal solutions for some instances of other problems.”

What’s all that mean? Well, suppose that a cashier owes a customer some change, and in that cashier’s drawer are quarters (25¢), dimes (10¢), nickels (5¢), and pennies (1¢). The problem to be solved is to decide which coins and how many of each to hand to the customer. 

Think of a “greedy” cashier as one who wants to take the biggest bite out of this problem as possible with each coin they take out of the drawer. For instance, if a customer is owed 41¢, the biggest first (i.e., best immediate, or local) bite that can be taken is 25¢. (That bite is “best” inasmuch as it gets us closer to 0¢ faster than any other coin would.) Note that a bite of this size would whittle what was a 41¢ problem down to a 16¢ problem, since 41 - 25 = 16. That is, the remainder is a similar but smaller problem. 

Needless to say, another 25¢ bite would be too big (assuming the cashier prefers not to lose money), and so our greedy cashier would move on to a bite of size 10¢, leaving them with a 6¢ problem. At that point, greed calls for one 5¢ bite followed by one 1¢ bite, at which point the problem is solved. The customer receives one quarter, one dime, one nickel, and one penny: four coins in total.

It turns out that this greedy approach (i.e., algorithm) is not only locally optimal but also globally so for America’s currency (and also the European Union’s). That is, as long as a cashier has enough of each coin, this largest-to-smallest approach will yield the fewest coins possible.

---

## How it Works
The program:
1. Prompts the user to input an integer representing the amount of change owed (in cents).
2. Uses a greedy algorithm to determine the fewest number of coins required (quarters, dimes, nickels, and pennies).
3. Outputs the minimum number of coins.

### Greedy Algorithm Explanation
The greedy algorithm works by always selecting the largest available coin denomination that does not exceed the remaining change. This ensures the least number of coins are given as change.

## Features
- Prompts the user for a valid amount of change owed.
- Continually asks for input until a valid integer greater than or equal to zero is entered.
- Outputs the minimum number of coins required to make the given change.

## Instructions

1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/your-username/CoinChanger.git

2. Navigate to the project directory:
   ```bash
   cd GreedyCash

3. Compile the code:
     ```bash
     make cash

4. Run the Program:
   ```bash
   ./cash

## Example Outputs

```bash

Input:
Change owed: 25
Output: 1


Input:
Change owed: 70
Output: 4


Input:
Change owed: 113
Output: 8
```

### Credits
Developed as part of the CS50 Introduction to Computer Science course by Harvard University.
Uses a greedy algorithm approach to solve the problem.


