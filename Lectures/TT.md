

# Lecture 2

## Document 1: Lecture 2 – Probability-Theoretic Foundations

**Slide 4 – Overview of random distributions** Left column: Discrete uniform / rectangular distribution; Binomial distribution; Poisson distribution; Erlang distribution; Engset distribution; Geometric distribution; Pascal distribution

Right column: Continuous uniform / rectangular distribution; Normal / Gaussian distribution; Standard normal distribution; Erlang distribution; Negative exponential distribution; (Hyperexponential, Hypoexponential, Erlang order k)

**Slide 5 – 2. Mathematical Foundations** The following mathematical foundations are assumed to be known:

**Classical probability theory** (Laplace event field)

- m possible and equally likely cases for occurrence or non-occurrence of event A
- g cases favorable for the occurrence of A, remaining m−g cases unfavorable

P[A] = g/m

But: equal likelihood of cases is not always given (e.g., a biased die)

Example: a) Should one bet for or against someone who claims to roll a 6 in 4 rolls of a die? b) Should one bet for or against someone who claims to roll a double-six in 24 rolls with 2 dice?

**Slide 6 – Modern probability theory: Axiomatic definitions (among others by Kolmogorov)** A **probability system** is characterized by:

a) the **sample space I** with **n elementary events** ωᵢ (i = 1,2,…,n) and the resulting set Z of all 2ⁿ possible random events

b) an **event field E={A,B,C}** as the set of at least all k random events of interest in connection with the trial, where event-algebraic operations must not lead out of E

c) the **probabilities assigned to the random events** Pⱼ (j = 1,2,…,k)

Examples: coin toss; dice (D4, D6, D10, D20, D100); n

**Slide 7 – Example of a probability system** Example: die Ideal Laplace die (D6) Suppose only whether an even or odd number is rolled is of interest. Event A … even // Event B … odd

E = {∅, A, B, I} k = 4 random events

Ā = B, B̄ = A A ∪ B = I, A ∩ B = ∅ Ī = 0, 0̄ = I

However, Z = 2⁶ = 64 random events would be possible.

Table (outcomes 1–6, rows = random events):

- Random event No. 1 (impossible event): 0 0 0 0 0 0
- Random event No. 2: 0 0 0 0 0 1
- …
- Random event No. 63: 1 1 1 1 1 0
- Random event No. 64 (certain event): 1 1 1 1 1 1

**Slide 8 – Axiomatic definitions of modern probability theory (among others by Kolmogorov)** **Axiom 1**: Assignment of event A → number P[A] **Axiom 2**: Certain event I with probability P[I] = 1 **Axiom 3**: P[A∪B∪C] = P[A]+P[B]+P[C] for pairwise mutually exclusive events **Axiom 4**: P[⋃ᵢ₌₁^∞ Aᵢ] = Σᵢ₌₁^∞ P[Aᵢ], (Aᵢ∩Aⱼ=∅, Aᵢ,Aⱼ∈E) for i≠j

Derivable: P[A∪B] = P[A]+P[B]−P[A∩B]

**Conditional probability**: P[A/B] = P[A∩B]/P[B] (≥ P[A∩B] by definition)

**Law of total probability**: P[B] = Σᵢ₌₁ⁿ P[B/Aᵢ]·P[Aᵢ]

**Bayes' theorem**: P[Aₖ/B] = P[Aₖ]/P[B] · P[B/Aₖ] = P[Aₖ]·P[B/Aₖ] / Σᵢ P[Aᵢ]·P[B/Aᵢ]

**Random variable X**: Assignment of elementary event ωᵢ → concrete value xᵢ of the variable X

(Diagram shows a Venn diagram with sample points ω₁,ω₂,ω₃,ω₄ in regions A, B, C, mapped down to values x₁,x₂,x₃,x₄ on axis X)

**Slide 9 – 2.1. Distribution and density functions** Distribution function / distribution probability distribution function (PDF) or cumulative distribution function (cdf)

F(x) = P[X ≤ x] → P[a < X ≤ b] = F(b) − F(a)

Properties:

1. F(−∞) = 0, F(∞) = 1, 0 ≤ F(x) ≤ 1
2. F(x₁) ≤ F(x₂) for x₁ ≤ x₂, i.e., non-decreasing
3. F(x₀) = lim_{h→0} F(x₀+h), i.e., right-continuous

**Slide 10 – Right-continuous vs. left-continuous**

|Right-continuous (used by us)|Left-continuous|
|---|---|
|F(x) = P[X ≤ x]|F(x) = P[X < x]|
|F(b)−F(a) = P[X≤b]−P[X≤a] = P[a<X≤b]|F(b)−F(a) = P[X<b]−P[X<a] = P[a≤X<b]|
|F(xᵢ) = P[X≤xᵢ]|F(xᵢ) = P[X<xᵢ]|
|F(xᵢ) = lim_{h→0} F(xᵢ+h)|F(xᵢ) = lim_{h→0} F(xᵢ−h)|

(Two step-function diagrams illustrating the open/closed circle convention at jump point xᵢ, height Pᵢ)

**Slide 11 – Density function** Density function / probability density / density probability density function (pdf) or frequency function

f(x) = F'(x) = dF(x)/dx ↔ P[X≤x] = F(x) = ∫₋∞ˣ f(t)dt

P[a<X≤b] = F(b)−F(a) = ∫ₐᵇ f(x)dx Probability that the random variable X falls in the half-open interval (a,b]

**Slide 12 – Properties of random variables** Properties:

1. f(x) = F'(x) ≥ 0
2. ∫₋∞^∞ f(x)dx = F(∞) = 1

P[X>x] = 1−F(x) = ∫ₓ^∞ f(t)dt = F̄(x)

Complementary distribution function, complementary PDF, complementary cumulative function, ccdf

Actually only defined for continuous random variables (because of dFₓ(x)/dx), but… Discrete random variables are treated as a special case of continuous ones → by using a "degenerate" density function for discrete random variables

**Slide 13 – Discrete random variable** (Diagrams: probability mass function P[X=x] with spikes 0.5, 0.2, 0.3 at x₁,x₂,x₃; corresponding step CDF F_X(x) rising to 0.5, 0.7, 1)

**Slide 14 – Discrete random variable** f_X(x) = P[X=x₁]·δ(x−x₁) + P[X=x₂]·δ(x−x₂) + P[X=x₃]·δ(x−x₃)

General: f_X(x) = Σᵢ P[X=xᵢ]·δ(x−xᵢ)

Sifting property of δ(x): ∫₋∞^∞ g(t)·δ(t−t₀)dt = g(t₀)

**Slide 15 – Exercise on the distribution function** Given: P[A]=p, occurrence of A → X=1, non-occurrence of A → X=0 Find: F(x), f(x)

Solution: F(x)=P[X≤x], P[X=1]=P[A]=p, P[X=0]=P[Ā]=1−p

F(x) = 0 for x<0; 1−p for 0≤x<1; 1 for 1≤x

f(x) = P[X=x₁]·δ(x−x₁) + P[X=x₂]·δ(x−x₂) = (1−p)·δ(x) + p·δ(x−1)

Also called the Bernoulli distribution; synonym: two-point distribution; special two-point distribution: zero-one distribution

**Slide 16** – (Comparison figure: distribution function, density function, and probability function for discrete RV (top row) vs. continuous RV (bottom row), no additional text)

**Slide 17 – Important probability distributions for discrete random variables**

1. Discrete uniform / rectangular distribution
2. Binomial distribution
3. Poisson distribution
4. Erlang distribution
5. Engset distribution

Geometric distribution Pascal distribution

**Slide 18 – 1. (Discrete) uniform distribution / (discrete) rectangular distribution** (Laplace distribution for discrete RVs ↔ Laplace die, beetle, wheel of fortune)

P[X=x] = 1/n for n outcomes of the RV X

F(x) = 0 for x<0; Σₖ₌₀ˣ 1/n for 0≤x≤n−1; 1 for n−1<x

P(k) = 1/n for k = 0,1,…,n−1

**Slide 19** – (Four plots illustrating the uniform distribution's CDF and PMF for different n: n=10, and comparison of n=10, n=5, n=2)

**Slide 20 – 2. Binomial distribution** P[X=xₖ=k] = C(n,k)·pᵏ·(1−p)ⁿ⁻ᵏ with 0<p<1, n∈ℕ, k=0,1,2,…,n

A binomially distributed RV X can be represented as the sum of n independent, identically "two-point-distributed" RVs Xᵢ (more precisely: 0-1 distributions): X = Σᵢ₌₁ⁿ Xᵢ

Inverse relation: The zero-one distribution can be interpreted as a binomial distribution with n=1.

F(x) = 0 for x<0; Σₖ₌₀ˣ C(n,k)pᵏ(1−p)ⁿ⁻ᵏ for 0≤x≤n; 1 for n<x

**Slide 21** – (Four plots of the binomial distribution's CDF and PMF, for p=0.5 and comparison p=0.1, 0.5, 0.9)

**Slide 22 – Bonus homework (JupyterHub)** Part 1: Using multiple slider functions, visualize the influence of the two parameters on the shape and course of the probability function and the cumulative distribution function of the binomial distribution.

**Slide 23 – Example on the binomial distribution** Switching network (Koppelfeld) with full accessibility, where:

- s … inbound (feeder) lines
- r … outbound (subscriber) lines
- traffic offered A (=C·t_m) (call intensity · mean call duration)

Occupancy probability of a source p (=A/s) for r ≥ s

The RV "number of (simultaneously) occupied outbound lines" (0≤x≤s) is binomially distributed.

Pₓ = P[X=x] = C(s,x)·pˣ·(1−p)ˢ⁻ˣ

(Diagram: matrix of s inbound lines × r outbound lines)

**Slide 24 – Traffic offered vs. traffic carried** What can be understood as the traffic offered A? → Mean number of desired connections

Traffic carried: mean number of simultaneously occupied lines / mean number of calls handled

Here: traffic offered = traffic carried (because r ≥ s), no losses!

Note: A = E[X] = n·p = A, for the binomial distribution where p = A/s and n = s

**Slide 25 – 3. POISSON distribution** Derived from the binomial distribution with n→∞, p→0, n·p = a (>0)

P[X=xₖ=k] = aᵏ/k! · e⁻ᵃ = (λt)ᵏ/k! · e⁻λt

In traffic theory often: a = λt

F(x) = 0 for x<0; Σₖ₌₀ˣ (λt)ᵏ/k! · e^(−λt) for 0≤x

**Slide 26** – (Four plots of the Poisson distribution's CDF and PMF, for λt=1.0 and comparison λt=0.3, 1.0, 3)

**Slide 27 – Examples on the Poisson distribution** Example 1: The number X of demands arriving at a service system within the time interval Δt is very often Poisson distributed, or is modeled as such:

P[X=k] = (λ·Δt)ᵏ/k! · e^(−λ·Δt)

(λ = mean number of demands per time unit)

Example 2: Switching network (see above) with s→∞ and r→∞, with traffic offered A (=traffic carried, because r→∞)

The RV "number X of (simultaneously) occupied outbound lines" (0≤x<∞) is Poisson distributed.

Pₓ = P[X=x] = Aˣ/x! · e⁻ᴬ

(Derivation later — see M/M/s service system or M/G/s service system)

**Slide 28 – Schedule** (same content as Slide 3)

**Slide 29** – Thank you.

---

## Document 2: Exercises 02 – Random distributions

**Page 1**

**1.)** Given: density function of the Erlang distribution of order k (for continuous random variables): f(x) = λᵏ x^(k−1) / (k−1)! · e^(−λx) (x ≥ 0; λ > 0, k = 1,2,3,…) Find: distribution function F(x)

**2.)** Given: n independent random variables X₁, X₂, …, Xₙ, each with f_Xᵢ(x) = λe^(−λx) for x≥0, 0 for x<0 (i = 1, 2, …, n) Find: distribution and density function of the random variable X = min(X₁, X₂, …, Xₙ)

**3.)** Given: independent random variables X₁, X₂, …, Xₙ; all Xᵢ identically exponentially distributed (see also problem 1!) Find: distribution and density function of the random variable X = max(X₁, X₂, …, Xₙ)

**4.)** Given: a switching facility with a very large number of inbound (feeder) lines (s→∞), 10 outbound lines, and full accessibility; traffic offered of 3 [Erlang] under pure-chance traffic type 1 (Erlang traffic). Find: the probability that 5 outbound lines are occupied; how large is the relative error that results if the calculation is carried out using the Poisson distribution instead?

**5.)** Given: an event stream with

- mutually independent
- identically distributed inter-event times T (f_T(y) = λe^(−λy) for y≥0), and
- guaranteed single arrivals; Find: the density function of the time interval X between a total of (k+1) events

**6.)** Given: simultaneous rolling of two ideal dice Find: the probability distribution (probability function and distribution function) of the sum of the pips X (x = 2, 3, …, 12)

**Page 2**

**7.)** Given: a bundle of 4 telephone lines; occupancy probability of a line: p = 1/6 Find: the probability that 0, 1, 2, 3, or 4 of these 4 lines are occupied

**8.)** Which distribution governs the inter-arrival time Tₐ for a Poisson stream?

**9.)** Which distribution governs the number X of demands occurring during the time interval Δt, if the inter-arrival times are independent, identically distributed (with f_Tₐ(t) = λe^(−λt)) and guaranteed to be > 0?

**10.)** Given: in a telephone exchange, a call stream with Poisson characteristics arrives with an average of 90 calls per minute. Find: the standard deviation (spread) of the inter-arrival time

**11.)** Given: a bundle of 10 telephone lines. The following occupancy state is observed (xᵢ = number of occupied lines in the bundle):

|xᵢ|0|1|2|3|4|5|6|7|8|9|10|
|---|---|---|---|---|---|---|---|---|---|---|---|
|P[X=xᵢ]|0.2|0.19|0.16|0.13|0.1|0.07|0.05|0.04|0.03|0.02|0.01|

Find:

1. The probability that any calls are taking place at all
2. The expected value of the number of occupied lines
3. The probability that the bundle is loaded to at most half capacity (no more than 50%), i.e., that at least 5 lines are free
4. The probability that no free line is found (= "danger time"/blocking time)
5. The distribution function F(x)

**Z1.)** Are trams with deterministic inter-arrival times (IAT) of 10 min "better" or "worse" than trams with uniformly distributed IAT between 5 min and 15 min??




