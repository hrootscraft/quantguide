**Medium** <br> 
A family has 2 children, of which we know one is a boy born on a Friday. Assuming that each birthday and gender is equally likely, as well as independent of one another, find the probability that the family has 2 boys. 
<br><br>

**Notes**<br>
**APPROACH 1: List Possible Probabilities**

We can list all possible scenarios for a family with 2 children, considering both gender and day of birth, then focus on those matching our condition.

Since one child is a boy born on Friday, let's enumerate all possible combinations where at least one child is a boy born on Friday:

First, let's establish our possibilities:
- Gender: Boy (B) or Girl (G) - 2 options
- Day: Friday (F) or Not-Friday (NF) - 2 options

Each child can be:
- Boy born on Friday (BF)
- Boy not born on Friday (BNF)
- Girl born on Friday (GF)
- Girl not born on Friday (GNF)

Child 1 can be:
- BF: probability 1/2 × 1/7 = 1/14
- BNF: probability 1/2 × 6/7 = 6/14
- GF: probability 1/2 × 1/7 = 1/14
- GNF: probability 1/2 × 6/7 = 6/14

Given our condition (at least one boy born on Friday), let's list all possible scenarios:
1. (BF, BF): Both boys born on Friday
2. (BF, BNF): First boy on Friday, second boy not on Friday
3. (BF, GF): First boy on Friday, second girl on Friday
4. (BF, GNF): First boy on Friday, second girl not on Friday
5. (BNF, BF): First boy not on Friday, second boy on Friday
6. (GF, BF): First girl on Friday, second boy on Friday
7. (GNF, BF): First girl not on Friday, second boy on Friday

The probability of each scenario is:
1. (BF, BF): (1/14) × (1/14) = 1/196
2. (BF, BNF): (1/14) × (6/14) = 6/196
3. (BF, GF): (1/14) × (1/14) = 1/196
4. (BF, GNF): (1/14) × (6/14) = 6/196
5. (BNF, BF): (6/14) × (1/14) = 6/196
6. (GF, BF): (1/14) × (1/14) = 1/196
7. (GNF, BF): (6/14) × (1/14) = 6/196

Total probability of these scenarios: 27/196

The favorable scenarios (both children are boys):
1. (BF, BF): 1/196
2. (BF, BNF): 6/196
5. (BNF, BF): 6/196

Total probability of favorable scenarios: 13/196

Therefore:
P(both children are boys | one is a boy born on Friday) = 13/196 ÷ 27/196 = 13/27

The probability is 13/27 (approximately 48.1%).
<br><br>

**APPROACH 2: Bayes' Theorem**

Bayes' theorem is:
<br>P(A|B) = [ P(B|A) × P(A) ] / P(B)

For our problem:
- A = "family has two boys"
- B = "at least one child is a boy born on Friday"

We need to find P(A|B) = P(two boys | one is a boy born on Friday).

Let's calculate each component:

1. P(A) = Probability of having two boys = 1/2 * 1/2 = **1/4**

2. P(B|A) = Probability that at least one child is a boy born on Friday, given both are boys
   - Using complementary probability rule,
     <br>Probability neither boy born on Friday = (6/7) × (6/7) = 36/49
   - Therefore, probability at least one boy born on Friday = 1 - 36/49 = **13/49**

3. P(B) = Total probability that at least one child is a boy born on Friday. Basically, we need the probability that a family with 2 children has at least one boy born on Friday, considering all possible gender combinations.

   *First, let's look at all possible gender combinations for 2 children:*
   <br>BB: Both children are boys (probability 1/4)
   <br>BG: First child is boy, second is girl (probability 1/4)
   <br>GB: First child is girl, second is boy (probability 1/4)
   <br>GG: Both children are girls (probability 1/4)

   *For each combination, what's the chance of having a boy born on Friday?*
   <br>BB: P(at least one boy on Friday) = 13/49
   <br>BG: P(boy on Friday) = 1/7
   <br>GB: P(boy on Friday) = 1/7
   <br>GG: P(boy on Friday) = 0
   
   So, P(B) = (1/4)(13/49) + (1/4)(1/7) + (1/4)(1/7) + (1/4)(0)
   <br>= 13/196 + 1/28 + 1/28 + 0
   <br>= 13/196 + 2/28
   <br>= 13/196 + 14/196
   <br>= 27/196

Now we can plug these values into Bayes' theorem:
<br>P(A|B) = P(B|A) × P(A) / P(B)
<br>= (13/49) × (1/4) / (27/196)
<br>= (13/49) × (1/4) × (196/27)
<br>= 13/49 × 196/108
<br>= 13 × 196 / 49 × 108
<br>= 13 × 196 / 5,292
<br>= 2,548 / 5,292
<br>= 13/27

Therefore, the probability that the family has two boys, given that one is a boy born on Friday, is 13/27.

**Why This Is a Paradox**
<br>The solution explains why this result (13/27 ≈ 48.1%) is higher than the unconditional probability of having two boys (1/4 = 25%). This is because knowing that at least one child is a boy born on Friday increases the likelihood that the family has two boys. With two boys, you have two chances to get a Friday birth, making this scenario more likely than having just one boy and one girl.
