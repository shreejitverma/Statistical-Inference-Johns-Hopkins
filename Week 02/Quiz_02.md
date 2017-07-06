Quiz 02
=======

<table>
<thead>
<tr class="header">
<th align="center">Attempts</th>
<th align="center">Score</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center">1/3</td>
<td align="center">8/8</td>
</tr>
</tbody>
</table>

Question 01
-----------

What is the variance of the distribution of the average an IID draw of n
observations from a population with mean *μ* and variance
*σ*<sup>2</sup>.

### Answer

*σ*<sup>2</sup>/n

Question 02
-----------

Suppose that diastolic blood pressures (DBPs) for men aged 35-44 are
normally distributed with a mean of 80 (mm Hg) and a standard deviation
of 10. About what is the probability that a random 35-44 year old has a
DBP less than 70?

### Answer

-   16%

#### Explanation

    pnorm(70, mean=80, sd=10)

    ## [1] 0.1586553

Question 03
-----------

Brain volume for adult women is normally distributed with a mean of
about 1,100 cc for women with a standard deviation of 75 cc. What brain
volume represents the 95th percentile?

### Answer

-   Approximately 1223.

#### Explanation

    qnorm(.95, mean=1100, sd=75)

    ## [1] 1223.364

Question 04
-----------

Refer to the previous question. Brain volume for adult women is about
1,100 cc for women with a standard deviation of 75 cc. Consider the
sample mean of 100 random adult women from this population. What is the
95th percentile of the distribution of that sample mean?

### Answer

-   Approximately 1112 cc.

#### Explanation

    qnorm(.95, mean=1100, sd=(75/sqrt(100)))

    ## [1] 1112.336

Question 05
-----------

You flip a fair coin 5 times, about what's the probability of getting 4
or 5 heads?

### Answer

-   19%

#### Explanation

    1 - pbinom(3, 5, .5)

    ## [1] 0.1875

Question 06
-----------

The respiratory disturbance index (RDI), a measure of sleep disturbance,
for a specific population has a mean of 15 (sleep events per hour) and a
standard deviation of 10. They are not normally distributed. Give your
best estimate of the probability that a sample mean RDI of 100 people is
between 14 and 16 events per hour?

### Answer

-   68%

#### Explanation

    sd <- 10 / sqrt(100)
    pnorm(16, mean=15, sd) - pnorm(14, mean=15, sd)

    ## [1] 0.6826895

Question 07
-----------

Consider a standard uniform density. The mean for this density is .5 and
the variance is 1 / 12. You sample 1,000 observations from this
distribution and take the sample mean, what value would you expect it to
be near?

### Answer

-   0.5

Question 08
-----------

The number of people showing up at a bus stop is assumed to be Poisson
with a mean of 5 people per hour. You watch the bus stop for 3 hours.
About what's the probability of viewing 10 or fewer people?

### Answer

-   0.12

#### Explanation

    ppois(10, 3*5)

    ## [1] 0.1184644
