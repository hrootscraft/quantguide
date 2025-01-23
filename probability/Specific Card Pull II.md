**Medium** <br> 
A deck of cards is shuffled well. The cards are dealt one-by-one, until the two of hearts appears. Find the probability that exactly one king, queen and jack appear before the two of hearts.
<br><br>

**Notes**<br>
```
_______    _______     _______     _______      _______     ......     _______
    K         Q           J         NonKQJ       NonKQJ     ......        2♡   

_______    _______     _______     _______      _______     _______
    K         Q           J         NonKQJ       NonKQJ       2♡   

_______    _______     _______     _______      _______
    K         Q           J         NonKQJ        2♡   

_______    _______     _______     _______ 
    K         Q           J           2♡   
```

Approach 2
Instead of caring how many NonKQJ cards come before 2♡ we can care how the remaining 3 KQJs are arranged after 2♡:

First, we identify the key cards we care about: all Kings (4), all Queens (4), all Jacks (4), and the 2♡ (1). That's 13 cards total.
For the condition "exactly one K, Q, J before 2♡" to be true:

We need to choose which King (4 choices) will be before 2♡
We need to choose which Queen (4 choices) will be before 2♡
We need to choose which Jack (4 choices) will be before 2♡
These three cards can be arranged in 3! = 6 ways before the 2♡
The remaining 9 cards (3K, 3Q, 3J) can be arranged in 9! ways after the 2♡


The total possible arrangements of these 13 cards is 13!
Therefore, the probability is:
(4 choices for K) × (4 choices for Q) × (4 choices for J) × (3! ways to arrange chosen KQJ) × (9! ways to arrange rest)
divided by
(13! total possible arrangements)
= (4 × 4 × 4 × 6 × 9!) / 13! = 16/715
