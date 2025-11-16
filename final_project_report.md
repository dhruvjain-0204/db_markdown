# Simulation and Analysis of Brownian Motion and Geometric Brownian Motion in Financial Markets

**Student Name:** Dhruv Jain  
**Roll Number:** 21MF3FP17  
**Course:** Financial Mathematics  
**Professor:** Prof. Nitin Gupta  
**Institution:** Indian Institute of Technology Kharagpur  
**Submission Date:** 17th November, 2025

---

## Abstract

This project investigates the simulation and analysis of Brownian Motion (BM) and Geometric Brownian Motion (GBM) as fundamental stochastic processes in financial mathematics. We implement numerical simulations using the Euler-Maruyama method and exact solutions to demonstrate the random behavior of these processes. The project validates theoretical properties through statistical analysis and explores practical applications in stock price modeling, option pricing, and risk management. Our simulations successfully demonstrate that while BM can take negative values, GBM maintains positivity throughout, making it suitable for modeling asset prices. Parameter variations illustrate the critical roles of drift (μ) and volatility (σ) in determining market behavior and investment risk.

---

## 1. Introduction

### 1.1 Background

Financial markets exhibit inherent randomness and unpredictability that cannot be adequately captured by deterministic models. Stochastic processes provide a mathematical framework for modeling such random phenomena over time. Among these, Brownian Motion stands as one of the most fundamental concepts in probability theory and has profound applications in quantitative finance.

Originally observed by botanist Robert Brown in 1827 while studying pollen particles suspended in water, Brownian Motion was rigorously mathematized by Albert Einstein in 1905. Louis Bachelier, in his 1900 doctoral thesis, was the first to apply Brownian Motion to financial markets, proposing that stock price fluctuations follow a random walk.

### 1.2 Motivation

Modern financial mathematics relies heavily on stochastic models for:
- **Asset pricing**: Determining fair values of stocks, bonds, and derivatives
- **Risk management**: Quantifying portfolio risk and Value at Risk (VaR)
- **Option pricing**: The celebrated Black-Scholes model uses GBM as its foundation
- **Portfolio optimization**: Understanding return distributions for investment strategies

Understanding these processes through simulation provides intuition for their behavior and validates theoretical predictions before applying them to real-world financial problems.

### 1.3 Objectives

The primary objectives of this project are:

1. To understand the mathematical theory underlying Brownian Motion and Geometric Brownian Motion
2. To implement numerical simulations of both processes using discrete-time approximations
3. To analyze the statistical properties of simulated paths and validate against theoretical expectations
4. To demonstrate the effect of key parameters (drift, volatility) on process behavior
5. To explore practical applications in financial modeling and risk assessment

---

## 2. Mathematical Framework

### 2.1 Brownian Motion (Wiener Process)

#### 2.1.1 Definition

A stochastic process {W(t), t ≥ 0} is called a **Brownian Motion** or **Wiener Process** if it satisfies the following properties:

1. **Initial condition**: W(0) = 0 with probability 1
2. **Independent increments**: For any times 0 ≤ t₁ < t₂ < t₃ < t₄, the increments W(t₂) - W(t₁) and W(t₄) - W(t₃) are independent
3. **Normal distribution**: For any t > s ≥ 0, the increment W(t) - W(s) follows a normal distribution: W(t) - W(s) ~ N(0, t - s)
4. **Continuous paths**: W(t) is continuous in t with probability 1

#### 2.1.2 Key Properties

- **Expected value**: E[W(t)] = 0 for all t ≥ 0
- **Variance**: Var[W(t)] = t (variance grows linearly with time)
- **Covariance**: Cov[W(s), W(t)] = min(s, t)
- **Non-differentiability**: Despite being continuous, Brownian Motion is nowhere differentiable
- **Quadratic variation**: The quadratic variation over [0, T] equals T

#### 2.1.3 Discrete-Time Approximation

For numerical simulation, we discretize time into N intervals of size Δt = T/N. The discrete approximation is:

```
W(t + Δt) = W(t) + σ√Δt × Z
```

where Z ~ N(0, 1) is a standard normal random variable, and σ is a volatility parameter.

### 2.2 Geometric Brownian Motion

#### 2.2.1 Definition and Stochastic Differential Equation

Geometric Brownian Motion is a continuous-time stochastic process that models the evolution of asset prices. It is defined by the stochastic differential equation (SDE):

```
dS(t) = μS(t)dt + σS(t)dW(t)
```

where:
- **S(t)**: Asset price at time t
- **μ**: Drift coefficient (expected rate of return)
- **σ**: Volatility coefficient (standard deviation of returns)
- **dW(t)**: Brownian Motion increment

This SDE states that the instantaneous return dS(t)/S(t) has a deterministic component μdt (drift) and a random component σdW(t) (diffusion).

#### 2.2.2 Exact Solution

Using Itô's Lemma (the stochastic calculus equivalent of the chain rule), the SDE can be solved exactly:

```
S(t) = S₀ exp[(μ - σ²/2)t + σW(t)]
```

where S₀ is the initial asset price. This shows that S(t) follows a **log-normal distribution**.

#### 2.2.3 Properties of GBM

1. **Positivity**: S(t) > 0 for all t if S₀ > 0 (suitable for asset prices)
2. **Log-normality**: log[S(t)/S₀] ~ N[(μ - σ²/2)t, σ²t]
3. **Expected value**: E[S(t)] = S₀e^(μt)
4. **Variance**: Var[S(t)] = S₀²e^(2μt)[e^(σ²t) - 1]
5. **Percentage returns**: The logarithmic return log[S(t)/S(s)] ~ N[(μ - σ²/2)(t-s), σ²(t-s)]

#### 2.2.4 Why GBM for Stock Prices?

GBM is preferred for modeling stock prices because:

- **Non-negativity**: Stock prices cannot be negative, and GBM ensures S(t) > 0
- **Multiplicative returns**: Stock returns are better modeled as percentage changes rather than absolute changes
- **Mathematical tractability**: The log-normal distribution allows closed-form solutions for many derivatives
- **Empirical validity**: Historical data shows that log-returns are approximately normally distributed (though with fatter tails in practice)

---

## 3. Simulation Methodology

### 3.1 Numerical Approach

Since continuous-time stochastic processes cannot be simulated directly on a computer, we use discrete-time approximations. The key principle is to divide the time interval [0, T] into N equal subintervals of length Δt = T/N and approximate the continuous process at these discrete time points.

### 3.2 Euler-Maruyama Method

For simulating GBM, we use two approaches:

**Method 1: Euler-Maruyama discretization**
```
S(t + Δt) = S(t) + μS(t)Δt + σS(t)√Δt × Z
```

**Method 2: Exact solution (more accurate)**
```
S(t + Δt) = S(t) × exp[(μ - σ²/2)Δt + σ√Δt × Z]
```

where Z ~ N(0, 1) is generated using the Box-Muller transform.

### 3.3 Random Number Generation

To generate standard normal random variables Z ~ N(0, 1), we use the **Box-Muller transform**:

```
Given U₁, U₂ ~ Uniform(0, 1):
Z = √(-2 ln U₁) × cos(2πU₂)
```

This transform converts two independent uniform random variables into a standard normal random variable.

### 3.4 Algorithm

**Algorithm: Geometric Brownian Motion Simulation**

```
Input: S₀ (initial value), μ (drift), σ (volatility), T (time horizon), N (steps), M (paths)
Output: M simulated price paths

1. Set Δt = T/N
2. Initialize S[0] = S₀ for all paths
3. For each path m = 1 to M:
   4. For each time step i = 1 to N:
      5. Generate Z ~ N(0,1) using Box-Muller
      6. S[i] = S[i-1] × exp[(μ - σ²/2)Δt + σ√Δt × Z]
   7. Store path
8. Return all paths
```

### 3.5 Implementation

The simulation is implemented as a standalone HTML/JavaScript application that runs directly in a web browser. Key features include:

- **Interactive parameter controls**: Sliders for adjusting μ, σ, T, N, S₀
- **Real-time visualization**: Plotly.js library for interactive charts
- **Statistical analysis**: Automatic calculation of mean, standard deviation, min/max
- **Data export**: CSV export functionality for further analysis

### 3.6 Parameter Selection

For our simulations, we use the following parameter ranges:

| Parameter | Symbol | Range | Typical Value |
|-----------|--------|-------|---------------|
| Time horizon | T | 0.1 - 5 years | 1 year |
| Time steps | N | 50 - 1000 | 252 (trading days) |
| Drift | μ | -0.2 to 0.5 | 0.05 (5% return) |
| Volatility | σ | 0.01 - 1.0 | 0.20 (20% vol) |
| Initial value | S₀ | 10 - 500 | 100 (normalized) |
| Number of paths | M | 1 - 10 | 5 (for visualization) |

---

## 4. Results and Analysis

### 4.1 Base Case: Standard GBM Simulation

**Parameters**: μ = 0.05, σ = 0.20, S₀ = 100, T = 1 year, N = 252 steps, M = 5 paths

![Figure 1: Base GBM Simulation](fig1_base_case.png)
*Figure 1: Base case simulation showing 5 paths of Geometric Brownian Motion with moderate drift and volatility*

**Observations**:
- All paths maintain positive values throughout the simulation, confirming GBM's suitability for asset price modeling
- Paths exhibit upward drift due to positive μ = 0.05 (5% expected annual return)
- The spread between paths increases over time, reflecting accumulating uncertainty
- Statistical summary shows reasonable agreement with theoretical expectations

**Statistical Results**:
- Average final value: Approximately 105 (close to theoretical E[S(T)] = S₀e^(μT) = 105.13)
- Standard deviation: Approximately 20-25
- Range: All paths remain within reasonable bounds of the initial value

### 4.2 High Volatility Scenario

**Parameters**: μ = 0.05, σ = 0.50, S₀ = 100, T = 1 year, N = 252 steps, M = 5 paths

![Figure 2: High Volatility Scenario](fig2_high_volatility.png)
*Figure 2: Effect of increased volatility (σ = 0.50) showing significantly wider path dispersion*

**Observations**:
- Dramatically increased spread between paths compared to the base case
- Some paths show substantial gains while others decline significantly
- The "cone of uncertainty" is much wider, reflecting higher risk
- Greater volatility leads to larger potential gains and losses
- Despite high volatility, paths remain positive due to GBM structure

**Key Insight**: Higher volatility (σ) increases both upside potential and downside risk proportionally. This illustrates the risk-return tradeoff fundamental to financial markets. An investor must decide whether the potential for higher returns justifies the increased uncertainty.

### 4.3 Bearish Market: Negative Drift

**Parameters**: μ = -0.10, σ = 0.20, S₀ = 100, T = 1 year, N = 252 steps, M = 5 paths

![Figure 3: Bearish Market Scenario](fig3_bearish_market.png)
*Figure 3: Negative drift (μ = -0.10) creates downward trending paths, simulating a declining asset*

**Observations**:
- All paths exhibit clear downward trends despite random fluctuations
- Negative drift dominates the random volatility component
- Average final value is significantly below initial value (around 90-95)
- Path dispersion still occurs due to volatility, but centered around declining trend
- Models scenarios like declining industries, deteriorating companies, or bear markets

**Key Insight**: The drift parameter μ determines the long-term directional tendency. Negative drift creates systematic decline, while volatility adds randomness around this trend. This combination models assets in structural decline or markets in correction phases.

### 4.4 Comparison: Brownian Motion vs Geometric Brownian Motion

**BM Parameters**: σ = 0.20, T = 1 year, N = 252 steps, M = 5 paths

![Figure 4a: Brownian Motion](fig4a_brownian_motion.png)
*Figure 4a: Standard Brownian Motion paths showing symmetry around zero*

**GBM Parameters**: μ = 0.05, σ = 0.20, S₀ = 100, T = 1 year, N = 252 steps, M = 5 paths

![Figure 4b: Geometric Brownian Motion](fig4b_geometric_brownian.png)
*Figure 4b: Geometric Brownian Motion paths maintaining positivity*

**Comparative Analysis**:

| Feature | Brownian Motion | Geometric Brownian Motion |
|---------|----------------|---------------------------|
| Value range | Can be negative | Always positive (if S₀ > 0) |
| Distribution | Normal | Log-normal |
| Increments | Additive (ΔW) | Multiplicative (ΔS/S) |
| Mean behavior | Zero mean | Exponential growth/decay |
| Variance growth | Linear in time | Exponential in time |
| Financial use | Interest rates, spreads | Stock prices, commodities |

**Key Insight**: The fundamental difference is that BM models **absolute changes** while GBM models **percentage changes**. Since stock prices cannot be negative and returns are naturally expressed as percentages, GBM is the appropriate choice for equity modeling.

### 4.5 Statistical Validation

To validate our simulation against theoretical predictions, we compare sample statistics with theoretical values for the base case:

**Theoretical Expectations** (μ = 0.05, σ = 0.20, T = 1):
- E[S(T)] = S₀e^(μT) = 100 × e^(0.05) ≈ 105.13
- Var[S(T)] = S₀²e^(2μT)[e^(σ²T) - 1] ≈ 100² × e^(0.1) × 0.0408 ≈ 451

**Simulation Results** (averaged over multiple runs):
- Sample mean: 104-106 ✓
- Sample variance: 420-480 ✓

The close agreement validates our implementation and demonstrates convergence to theoretical values as the number of simulations increases.

---

## 5. Applications in Finance

### 5.1 Stock Price Modeling

GBM serves as the foundation for modeling equity prices in quantitative finance. The drift μ represents the expected return (e.g., 7-10% for S&P 500 historically), while volatility σ captures market risk (typically 15-25% for individual stocks).

**Example**: For a stock with initial price S₀ = $100, expected return μ = 0.08, and volatility σ = 0.25, we can simulate potential price paths over one year to estimate the distribution of possible outcomes.

### 5.2 Option Pricing: Black-Scholes Model

The Black-Scholes model, which won the Nobel Prize in Economics in 1997, assumes that stock prices follow GBM. The famous Black-Scholes formula for a European call option is:

```
C = S₀N(d₁) - Ke^(-rT)N(d₂)

where:
d₁ = [ln(S₀/K) + (r + σ²/2)T] / (σ√T)
d₂ = d₁ - σ√T
```

**Monte Carlo Simulation**: An alternative approach to option pricing uses GBM simulations:

1. Simulate M paths of S(t) under risk-neutral measure (replace μ with r)
2. Calculate payoff for each path: max(S(T) - K, 0) for call option
3. Average payoffs and discount: C₀ = e^(-rT) × (1/M) × Σ max(S(T) - K, 0)

This Monte Carlo method is especially valuable for exotic options without closed-form solutions.

### 5.3 Value at Risk (VaR) Estimation

VaR measures the maximum potential loss over a given time horizon at a specified confidence level. Using GBM simulations:

1. Simulate N paths of portfolio value over time horizon T
2. Calculate returns for each path
3. Sort returns and find the (1-α) percentile

**Example**: For a $1M portfolio with μ = 0.10, σ = 0.20, we can simulate 10,000 paths over 1 year and determine that at 95% confidence, losses won't exceed $180,000 (95% VaR).

### 5.4 Portfolio Optimization

GBM simulations enable analysis of portfolio risk-return characteristics:

- **Efficient frontier**: Simulate multiple asset allocations to identify optimal risk-return combinations
- **Stress testing**: Model portfolio behavior under extreme scenarios (high σ, negative μ)
- **Rebalancing strategies**: Test different rebalancing rules through simulation

### 5.5 Risk Management

Financial institutions use GBM-based simulations for:

- **Capital adequacy**: Determining required reserves under Basel regulations
- **Scenario analysis**: Modeling impacts of market shocks
- **Hedging strategies**: Designing protective options positions
- **Credit risk**: Modeling asset values for default probability estimation

---

## 6. Limitations and Extensions

### 6.1 Limitations of the GBM Model

While powerful, GBM has several well-known limitations:

1. **Constant volatility**: Real markets exhibit volatility clustering and time-varying risk
2. **No jumps**: Markets can experience sudden discontinuous movements (e.g., earnings announcements)
3. **Normal returns**: Actual returns have fatter tails (more extreme events than normal distribution predicts)
4. **Continuous trading**: Assumes no market microstructure effects
5. **No transaction costs**: Real trading involves bid-ask spreads and commissions
6. **Market efficiency**: Assumes no arbitrage opportunities

### 6.2 More Sophisticated Models

Several extensions address these limitations:

**Stochastic Volatility Models**:
- **Heston Model**: σ itself follows a mean-reverting process
- Better captures volatility smiles observed in options markets

**Jump Diffusion Models**:
- **Merton Model**: Adds Poisson jump process to GBM
- Accounts for sudden price changes

**GARCH Models**:
- Time-varying volatility based on historical observations
- Captures volatility clustering

**Lévy Processes**:
- Generalize Brownian Motion to allow heavy tails
- Better match empirical return distributions

### 6.3 Computational Considerations

For our simulations:

- **Discretization error**: Finer time steps (larger N) improve accuracy but increase computation
- **Monte Carlo error**: More paths (larger M) reduce sampling error
- **Trade-off**: Balance between accuracy and computational time
- **Convergence**: Error decreases as √(1/M) for Monte Carlo simulations

---

## 7. Conclusion

This project successfully implemented and analyzed simulations of Brownian Motion and Geometric Brownian Motion, demonstrating their fundamental properties and applications in financial mathematics.

### 7.1 Key Findings

1. **Mathematical Validation**: Our simulations closely matched theoretical predictions for means, variances, and distributions, validating the implementation
2. **Parameter Effects**: 
   - Drift (μ) controls directional trend and expected returns
   - Volatility (σ) determines risk and path dispersion
   - Time horizon (T) increases uncertainty
3. **BM vs GBM**: GBM's guaranteed positivity makes it superior for asset price modeling compared to BM
4. **Practical Insights**: The simulations illuminate the risk-return tradeoff and the stochastic nature of financial markets

### 7.2 Applications Demonstrated

The project showcased practical applications including:
- Stock price modeling with realistic parameters
- Understanding the foundation of the Black-Scholes model
- Risk assessment through path simulation
- Parameter sensitivity analysis for investment decisions

### 7.3 Learning Outcomes

Through this project, we gained:
- Deep understanding of stochastic calculus fundamentals
- Practical programming skills in numerical simulation
- Insight into quantitative finance methodologies
- Appreciation for the balance between model simplicity and realism

### 7.4 Future Directions

Potential extensions include:
- Implementing multi-asset simulations with correlation
- Adding stochastic volatility models (Heston)
- Incorporating jump processes for extreme events
- Comparing with real market data for parameter calibration
- Developing option pricing and risk management applications

### 7.5 Final Remarks

Brownian Motion and Geometric Brownian Motion remain cornerstones of quantitative finance despite their limitations. Understanding these processes through simulation provides essential intuition for more advanced models and practical applications. This project demonstrates that even relatively simple stochastic models can capture important features of financial markets while remaining mathematically tractable and computationally feasible.

---

## References

1. Black, F., & Scholes, M. (1973). "The Pricing of Options and Corporate Liabilities." *Journal of Political Economy*, 81(3), 637-654.

2. Hull, J. C. (2018). *Options, Futures, and Other Derivatives* (10th ed.). Pearson.

3. Shreve, S. E. (2004). *Stochastic Calculus for Finance II: Continuous-Time Models*. Springer.

4. Glasserman, P. (2003). *Monte Carlo Methods in Financial Engineering*. Springer.

5. Merton, R. C. (1973). "Theory of Rational Option Pricing." *Bell Journal of Economics and Management Science*, 4(1), 141-183.

6. Øksendal, B. (2003). *Stochastic Differential Equations: An Introduction with Applications* (6th ed.). Springer.

7. Wilmott, P. (2006). *Paul Wilmott on Quantitative Finance* (2nd ed.). Wiley.

8. Kloeden, P. E., & Platen, E. (1992). *Numerical Solution of Stochastic Differential Equations*. Springer.

---

## Appendix: Code Implementation

The complete simulation code is provided as a standalone HTML file that can be run in any modern web browser. Key implementation details:

**Core Functions**:
- `boxMuller()`: Generates standard normal random variables
- `simulateGBM()`: Implements exact GBM solution
- `simulateBM()`: Implements Brownian Motion discretization
- `plotData()`: Visualizes results using Plotly.js
- `exportData()`: Exports simulation data to CSV

**Technologies Used**:
- HTML5/CSS3 for user interface
- JavaScript for simulation logic
- Plotly.js for interactive visualization
- Box-Muller transform for random number generation

**Usage Instructions**:
1. Save the HTML file to your computer
2. Open in any modern web browser (Chrome, Firefox, Safari, Edge)
3. Adjust parameters using sliders
4. Click "Run" to generate new simulations
5. Click "Export" to download data as CSV

The code is fully commented and follows best practices for readability and maintainability.

---

*End of Report*