### Standard Full House Probability in Blackjack

**Notes**

The total number of 5-card full house hands is:

$$
\binom{13}{1} \cdot \binom{4}{3} \cdot \binom{12}{1} \cdot \binom{4}{2} 
= 13 \cdot 4 \cdot 12 \cdot 6 = 3744
$$

- `C(13, 1)`: choose rank for triple  
- `C(4, 3)`: choose 3 suits for the triple  
- `C(12, 1)`: choose different rank for the pair  
- `C(4, 2)`: choose 2 suits for the pair  

---

Total number of 5-card poker hands:

$$
\binom{52}{5} = 2,598,960
$$

---

So the probability of **any full house** is:

$$
\frac{3744}{2598960} \approx 0.001440576
$$
