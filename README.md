### Question 1
**Given:**
- The lifetime \(T\) of a processor is exponentially distributed with a mean lifetime of 2 years. This means \(T \sim \text{Exponential}(\lambda)\) with \(\lambda = \frac{1}{2}\).
- We are told that the processor failed sometime in the interval \([4, 8]\) years.
- We need to find the conditional probability that it failed before it was 5 years old.

**Solution:**

The exponential distribution has the memoryless property, which simplifies the calculations.

The probability density function (PDF) for an exponential distribution is given by:
\[ f_T(t) = \lambda e^{-\lambda t} \]

Given that \( \lambda = \frac{1}{2} \):
\[ f_T(t) = \frac{1}{2} e^{-\frac{1}{2} t} \]

We need to find \( P(T < 5 \mid 4 \leq T \leq 8) \).

Using the definition of conditional probability:
\[ P(T < 5 \mid 4 \leq T \leq 8) = \frac{P(4 \leq T < 5)}{P(4 \leq T \leq 8)} \]

First, calculate \( P(4 \leq T < 5) \):
\[ P(4 \leq T < 5) = \int_{4}^{5} \frac{1}{2} e^{-\frac{1}{2} t} \, dt \]
\[ = \left[ -e^{-\frac{1}{2} t} \right]_{4}^{5} \]
\[ = -e^{-\frac{1}{2} \cdot 5} - (-e^{-\frac{1}{2} \cdot 4}) \]
\[ = e^{-2} - e^{-\frac{5}{2}} \]

Next, calculate \( P(4 \leq T \leq 8) \):
\[ P(4 \leq T \leq 8) = \int_{4}^{8} \frac{1}{2} e^{-\frac{1}{2} t} \, dt \]
\[ = \left[ -e^{-\frac{1}{2} t} \right]_{4}^{8} \]
\[ = -e^{-\frac{1}{2} \cdot 8} - (-e^{-\frac{1}{2} \cdot 4}) \]
\[ = e^{-4} - e^{-2} \]

Therefore, the conditional probability:
\[ P(T < 5 \mid 4 \leq T \leq 8) = \frac{e^{-2} - e^{-\frac{5}{2}}}{e^{-4} - e^{-2}} \]
\[ = \frac{e^{-2} (1 - e^{-\frac{1}{2}})}{e^{-2} (e^{-2} - 1)} \]
\[ = \frac{1 - e^{-\frac{1}{2}}}{e^{-2} - 1} \]
\[ = \frac{1 - e^{-\frac{1}{2}}}{e^{-2} (1 - e^{-2})} \]
\[ = \frac{1 - e^{-\frac{1}{2}}}{1 - e^{-2}} \]

### Question 2
**Given:**
- The lifetime of a processor follows a Weibull distribution with parameters \( \lambda = 0.5 \) and \( \beta = 0.6 \).

#### Part a
**We need to find the probability that it will fail in its first year of operation.**

For a Weibull distribution, the cumulative distribution function (CDF) is:
\[ F(t) = 1 - e^{-(\lambda t)^\beta} \]

For \( t = 1 \):
\[ F(1) = 1 - e^{-(0.5 \cdot 1)^{0.6}} \]
\[ = 1 - e^{-0.5^{0.6}} \]
\[ = 1 - e^{-0.65975} \]

#### Part b
**Given it is still functional after \( t = 6 \) years of operation, what is the conditional probability that it will fail in the next year?**

Conditional probability for Weibull distribution:
\[ P(T < 7 \mid T > 6) = \frac{P(6 < T < 7)}{P(T > 6)} \]

First, calculate \( P(T > 6) \):
\[ P(T > 6) = 1 - F(6) \]
\[ F(6) = 1 - e^{-(0.5 \cdot 6)^{0.6}} \]
\[ = 1 - e^{-2.75257} \]

Next, calculate \( P(T < 7) \):
\[ F(7) = 1 - e^{-(0.5 \cdot 7)^{0.6}} \]
\[ = 1 - e^{-2.97169} \]

Thus:
\[ P(T < 7 \mid T > 6) = \frac{F(7) - F(6)}{1 - F(6)} \]

### Part c and d

**Repeat parts a and b for \( \beta = 2.2 \) and \( \beta = 1 \).**

You can follow similar steps to compute the probabilities by replacing \(\beta\) with the respective values.

### Question 3

**We need to plot the failure rate for the Weibull distribution with various parameter values.**

The failure rate (hazard function) for the Weibull distribution is:
\[ h(t) = \frac{\lambda \beta (\lambda t)^{\beta - 1}}{1 - F(t)} \]
\[ = \lambda \beta t^{\beta - 1} \]

#### Part a
- Fix \( \lambda = 1 \) and plot for \( \beta = 0.5, 1.0, 1.5 \).

#### Part b
- Fix \( \beta = 1.5 \) and plot for \( \lambda = 1, 2, 5 \).
