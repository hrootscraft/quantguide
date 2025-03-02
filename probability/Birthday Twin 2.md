**Medium** <br> 
Assuming 365 days in a year, hoW many people do we need in a class to make the probability that at least two people have the same birthday more than 1/2?
2<br><br>

**Notes**<br>
_When calculating probabilities for "at least" scenarios, you can use the complementary approach, which often simplifies calculations. Here's a general formula:
P(at least one event occurs) = 1 - P(none of the events occur)_

In our case, 
<br>P(atleast 2 share a day) 
<br>= 1 - P(none of them share a day ie all of them have distinct days) 

<br> Given P(atleast 2 share a day) > 1/2, P(none of them share a day ie all of them have distinct days) has to be < 1/2.
<br> Now let there be n people in the class, then the probability of each of them having distinct birthdays is
<br> 365/365 * 364/365 * 363/364 * ... * [365-(n-1)]/365

Therefore, now we solve this: 
<br> (365/365) × (364/365) × ... × (365-(n-1))/365 < 1/2
<br> ln[(365/365) × (364/365) × ... × (365-n+1)/365] < ln(1/2)
<br> ln(365/365) + ln(364/365) + ... + ln((365-n+1)/365) < -ln(2)
<br> ln(364/365) + ln(363/365) + ... + ln((365-n+1)/365) < -ln(2) since ln(1) = 0

We can approximate this using:
ln(1-x) ≈ -x for small x

So ln((365-k)/365) ≈ -k/365

Adding these up:
<br> -(1 + 2 + ... + (n-1))/365 < -ln(2)
<br> -(n-1)(n)/2/365 < -ln(2)
<br> (n-1)(n)/2/365 > ln(2)
<br> n(n-1) > 2(365)ln(2)
<br> n(n-1) > 2(365)(0.693) ≈ 506

Now we need the smallest n where n(n-1) > 506:
<br>For n = 22: 22(21) = 462 < 506
<br>For n = 23: 23(22) = 506 < 506 (approximately equal)
<br>For n = 24: 24(23) = 552 > 506

Therefore, n = 23 is the smallest value that makes the probability greater than 1/2.
