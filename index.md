---
title       : A Derivative Financial Instrument
subtitle    : Pricing a Call Option with Two Step Binomial Model
author      : Robby Twesten & Tristan Dillman McDougall 
job         : RT Financials
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax, bootstrap]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Preparing R-programming environment

```r
require(stringr)
require(slidify)
require(knitr)
require(DiagrammeR)
```

---
## Tools from AP Calculus

### Total Derivative
#### Stochastic Processes
##### Stochastic processes are observations whose value is random with respect to time

* Ito's Lemma


### Definition of e
#### Applications
* Future Value of Money
* Discount Rate

--- .class #id 
## Tools from Probability

### Binomial Distribution
1. $E[X] = n p$
2. $Var(X) = n p(1 - p)$

---
## Risk Neutral Valuation

### Assumptions
1. The expected return on a stock (or any other investment) is the risk-free rate.
2. The discount rate used for the expected payoff on an option (or any other instrument) is the risk-free rate.

### Purpose
1. Risk Neutral Valuation (RVN) simplifies pricing.

    All returns and discounts are at risk-free rate.
    
2. Relationship between stock and derivative is the same regardless of risk.

    Risk incorporated into price of stock.
    
---

## Stochastic Processes

### Stochastic processes are observations whose value is random with respect to time.

---

### Markov Process
* Markov process with respect to stock price implies that future price only depends on current price.
* Distribution is normal

    Means are additive and variances are additive
    
---

#### Wiener Process
* Distribution is standard normal, i.e. mean = 0 and variance = 1.

    A physical example of a Wiener processes is Brownian motion.
    
    $Var(X) = E[X^2] - (E[X])^2$
   
* Two properties are:
1.  The change $\Delta z$ during a small period of time $\Delta t$ is $\Delta z = \epsilon \sqrt(\Delta t)$ where $\epsilon$ is a standard normal distribution $\Phi(0,1)$.
2.  The values of $\Delta z$ for any two different short intervals of time, $\Delta t$, are independent.
