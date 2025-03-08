# **Pension Pricing Using Stochastic Models**
*Understanding How Actuaries Use Stochastic Processes for Pricing Pensions*

---

## **1. Introduction**
Pension pricing is a core responsibility of actuaries, ensuring that pension funds remain solvent while meeting their long-term liabilities. Unlike deterministic models, **stochastic models** provide a **probabilistic view** of uncertainties in pension funds.

Actuaries use **stochastic processes** to model:
- **Investment risk** (returns on pension assets).
- **Interest rate fluctuations** (impacting liability valuation).
- **Mortality & longevity risk** (estimating how long retirees will live).
- **Macroeconomic effects** (inflation, wages, and economic cycles).

To address these risks, actuaries rely on **two key categories of models**:
1. **Interest Rate & Investment Models** – Used to model investment returns, discount liabilities, and analyze macroeconomic factors.
2. **Mortality & Longevity Models** – Used to estimate life expectancy, mortality rates, and longevity risk in pension funds.

---

## **2. Interest Rate & Investment Models**
These models are used to **project future investment returns, interest rates, and macroeconomic conditions**, which impact pension fund solvency.

### **2.1 Geometric Brownian Motion (GBM) – Investment Returns**
#### **Why is it used?**
Pension funds **invest in stocks, bonds, and assets**. Since asset prices fluctuate, actuaries use **GBM**, a stochastic model where prices evolve based on randomness.

#### **Formula:**
$$
dS_t = \mu S_t dt + \sigma S_t dW_t
$$

Where:
- $\( S_t \)$ = Asset value at time $\( t \)$.
- $\( \mu \)$ = Expected return.
- $\( \sigma \)$ = Volatility.
- $\( W_t \)$ = Wiener process (random Brownian motion).

#### **How It Relates to Pension Pricing:**
- Used in **Monte Carlo simulations** to predict pension fund growth.
- Helps actuaries **evaluate fund solvency** under uncertainty.

---

### **2.2 Vasicek Model – Interest Rate Dynamics**
#### **Why is it used?**
Pension liabilities are discounted using **interest rates**, which fluctuate over time. The **Vasicek model** captures **mean reversion** (interest rates return to a long-term average).

#### **Formula:**
$$
dr_t = a(b - r_t)dt + \sigma dW_t
$$

Where:
- $\( r_t \)$ = Interest rate at time $\( t \)$.
- $\( a \)$ = Speed of reversion.
- $\( b \)$ = Long-term equilibrium rate.
- $\( \sigma \)$ = Volatility.

#### **How It Relates to Pension Pricing:**
- Used for **discounting future pension liabilities**.
- Helps estimate **bond yields**, which impact pension investments.

---

### **2.3 Cox-Ingersoll-Ross (CIR) Model – Stochastic Interest Rates**
#### **Why is it used?**
The Vasicek model **can produce negative interest rates**, which is unrealistic. The **CIR model** ensures **non-negative interest rates**.

#### **Formula:**
$$
dr_t = a(b - r_t)dt + \sigma \sqrt{r_t} dW_t
$$

The **$\( \sqrt{r_t} \)$** term ensures interest rates **never go negative**.

#### **How It Relates to Pension Pricing:**
- **Improves valuation of pension liabilities** using realistic rate paths.
- Used in **bond and annuity pricing** for pension funds.

---

### **2.4 Vector Auto Regression (VAR) – Economic Dependencies**
#### **Why is it used?**
Economic factors like **inflation, wages, and GDP** affect pension funds. **VAR** models how **multiple economic variables interact** over time.

#### **Formula:**
$$
Y_t = A_1 Y_{t-1} + A_2 Y_{t-2} + \dots + A_p Y_{t-p} + \epsilon_t
$$

Where:
- $\( Y_t \)$ = Vector of economic variables (inflation, interest rates, etc.).
- $\( A_i \)$ = Coefficient matrices.
- $\( \epsilon_t \)$ = Error term.

#### **How It Relates to Pension Pricing:**
- Predicts how **economic shocks** affect pension funds.
- Helps set **contribution rates** based on wages and inflation.

---

## **3. Mortality & Longevity Models**
These models help actuaries **forecast how long retirees will live**, which is crucial for pension pricing. They ensure that pensions are **funded adequately for future payouts**.

### **3.1 Lee-Carter Model – Mortality Rate Forecasting**
#### **Why is it used?**
Pension funds **pay out benefits until retirees pass away**. The **Lee-Carter model** forecasts **mortality rates** based on historical trends.

#### **Formula:**
$$
\ln m_x(t) = a_x + b_x k_t + \epsilon_{x,t}
$$

Where:
- $\( m_x(t) \)$ = Mortality rate at age $\( x \)$.
- $\( a_x \)$ = Average log mortality for age \( x \).
- $\( b_x \)$ = Sensitivity of age \( x \) to mortality trends.
- $\( k_t \)$ = Stochastic trend in mortality rates.

#### **How It Relates to Pension Pricing:**
- Helps estimate **life expectancy**, which determines **pension payouts**.
- Used to price **annuities and pension liabilities**.

---

### **3.2 Cairns-Blake-Dowd (CBD) Model – Longevity Risk**
#### **Why is it used?**
Pension funds **lose money** if retirees live **longer than expected**. The **CBD model** predicts **future longevity trends**.

#### **Formula:**
$$
\ln \left( \frac{q_x}{1 - q_x} \right) = \beta_0(t) + \beta_1(t)(x - \bar{x})
$$

Where:
- $\( q_x \)$ = Probability of death at age $\( x \)$.
- $\( \beta_0(t) \)$ = Base mortality level.
- $\( \beta_1(t) \)$ = Age-dependent mortality trend.

#### **How It Relates to Pension Pricing:**
- **Improves longevity risk assessment**.
- Helps adjust **annuity prices dynamically**.

---

## **4. Conclusion**
Stochastic models provide actuaries with powerful tools to **price pensions accurately** by **accounting for uncertainty**. By integrating these models, actuaries can ensure **pension funds remain solvent in the long run**.




---
# **Investment and Benefit Modeling in a Defined Contribution (DC) Pension Scheme**  
*Analyzing the Impact of Contributions, Investment Returns, and Guarantees*  

---

## **1. Introduction**  
In a **Defined Contribution (DC) Pension Scheme**, retirement benefits result from the interaction of three key processes:  
1. **Accumulation of Contributions** – Regular or lump-sum payments into the pension fund.  
2. **Investment Returns** – Growth of the pension fund based on investment strategy.  
3. **Minimum Guarantees** – Optional guarantees either **before retirement** (on lump sums) or **after retirement** (on annuities).  

The challenge is to determine an **optimal investment strategy** that balances **risk and return** while ensuring that pension liabilities are adequately funded.  

---

## **2. Problem Definition**  
Consider a **Defined Contribution (DC) pension scheme** with the following characteristics:  

### **2.1 Pension Scheme Type**  
- **Defined Contribution (DC)**: Benefits depend on accumulated contributions and investment returns.  
- **Retirement Benefits**: Paid either as a **lump sum** or as **annuities**.  

---

### **2.2 Contributions**  
- **Single Contribution**: A one-time payment at $\( t = 0 \)$.  
- **Continuous Contributions**: Regular payments made over time, modeled as a **stochastic cash flow**.  

---

### **2.3 Investment Policy**  
- **Objective**: Find the **best investment strategy** for assets backing pension liabilities.  
- **Investment applies both before and after retirement**.  

$$
dS_t = \mu S_t dt + \sigma S_t dW_t
$$  

Where:  
- $\( S_t \)$ = Pension fund value at time \( t \).  
- $\( \mu \)$ = Expected return (drift).  
- $\( \sigma \)$ = Volatility of returns.  
- $\( W_t \)$ = Brownian motion.  

---

### **2.4 Liabilities After Retirement**  
- Benefits are either **paid directly** or as an **annuity for \( T \) years**.  
- **Mortality is not considered** (fixed annuity period).  
- The **annuity level** is chosen by the retiree but must maintain **actuarial equilibrium**:  

$$
A(T) = \frac{F(T)}{\sum_{t=0}^{T} e^{-rt}}
$$  

Where:  
- $\( A(T) \)$ = Annuity payout per year.  
- $\( F(T) \)$ = Reserve fund at retirement.  
  
---

## **3. Investment Options and Risk Management**  

### **3.1 Investment Options Before Retirement**  
- Before retirement age, the contributions can be invested in a **Riskless Asset** or in a **Risky Asset**.
- The **Financial Risk** is therefore completely supported by the **Affiliate** who is also supposed to be responsible for its own **Investment Strategy**.
- In order to measure its preferences in terms of risk and return,the affiliate is a assumed to use a **Utility Function.**

$$
dS_t = (r_s - \delta) S_t dt + \sigma S_t dW_t
$$  

Where:  
- $\( r_s \)$ = Risky asset return.  
- $\( \delta \)$ = Dividend yield.  
- $\( \sigma \)$ = Volatility.  

---

### **3.2 Post-Retirement Investment Strategy** 
At retirement age this reserve is partly used during $\( T \)$ years to pay continuous constant revenue. 
The surplus after T years can be used by the affiliate to purchase a new annuity for a new period of $\( T \)$ years or can be directly paid. 
In this period, the financial risk is also supported by the affiliate. 


---

### **4. Elements of a Stochastic Optimal Control Problem**
We define a **stochastic optimal control problem** based on the following elements:  

1. **State variable**  
2. **Decision variable**  
3. **Evolution equation**  
4. **Objective function**  

---

### **4.1 State Variable**  
We choose as the state variable the market value of the pension account of the affiliate, denoted by $\( F(t) \)$ ("the fund") and modeled by a **continuous-time stochastic process**.


---

### **4.2 Decision Variable**  
- We will assume there are two assets in which the contributions can be invested:
  - **Risk-free asset**
    The risk-free asset denoted by Z(t) satisfies the ordinary differential equation:
    

$$
dZ(t) = r Z(t) dt
$$

with initial condition:

$$
Z(0) = 1
$$

where $\( r \)$ is the constant risk-free rate
    
  - **Risky asset**
    The risky asset denoted by $\( S(t) \)$ satisfies the stochastic differential equation:

$$
dS(t) = \delta S(t) dt + \sigma S(t) dw(t)
$$

with initial condition:

$$
S(0) = 1
$$

where:  
- $\( \delta \)$ = Constant mean return of the risky asset.  
- $\( \sigma \)$ = Constant volatility of the risky asset.  
- $\( W(t) \)$ = **Standard Brownian motion**.

    
---
### **4.3 Evolution Equations**  

The evolution of the state variable $\( F \)$ is determined by the financial strategy and by a contribution function denoted by $\( \pi(t) \)$ representing the cash in (or out if negative); this general function could represent, as well, contributions paid to the account (accumulation phase) as benefits paid by the pension account (decumulation phase). In this model, this function is assumed to be deterministic.

The fund $\( F \)$ is then the solution of the stochastic differential equation:

$$
dF(t) = (u(t) \delta + (1 - u(t)) r) F(t) dt + \pi(t) dt + u(t) \sigma F(t) dw(t)
$$

$$
F(0) = P
$$

$$
(0 \leq t \leq N)
$$

where:

- $\( P \)$ = initial value of the account;  
- $\( N \)$ = time horizon considered.

The initial value of the account must be sufficient to finance the eventual deficit of the cash function in present value. So we will add the following constraint on the parameters:

$$
F(0) + \int_{0}^{N} \pi(s) e^{-rs} ds \geq 0
$$

---

### **4.4 The Objective Function** 
The goal of the affiliate is to maximize the expected utility of its terminal wealth at time \( t = N \). The utility function of the affiliate will be denoted by \( U \). So the optimal control problem is:

$$
\max_{u} \quad \mathbb{E} \big( U(F(N)) \big)
$$



### **5. Optimization Problem**  
The objective is to **determine the optimal proportion $\( u(t) \)$** to invest in the **risky asset $\( S(t) \)$**, while the remaining proportion $\( 1 - u(t) \)$ is invested in the **risk-free asset $\( Z(t) \)$**.  


---

---

## **Solution Approach**  

### **Value Function Definition**  
As is common in **stochastic optimal control**, we define the **value function** as:

$$
W(t, F) = \max_{u} \mathbb{E} \left[ U(F(N)) | F(t) = F \right]
$$

---

## **Applying the Maximum Principle**  

### **Hamilton-Jacobi Relation**  
From the **maximum principle** (Section 3.4), we obtain the **Hamilton-Jacobi-Bellman (HJB) equation**:

$$
0 = \max_{u} \left\{ \frac{\partial W}{\partial t} + \left( (u(t)(\delta - r) + r)F + \pi(t) \right) \frac{\partial W}{\partial F} + \frac{1}{2} u^2 (t) \sigma^2 F^2 \frac{\partial^2 W}{\partial F^2} \right\}
$$
 

At the **optimal control** $\( u^* \)$, we must satisfy:

$$
\Psi (u^*) = 0
$$

and  

$$
\frac{\partial \Psi}{\partial u} (u^*) = 0
$$


---

### **Optimal Investment Strategy \( u^* \)**  

From the **HJB equation**, we derive a semi-explicit formula for the **optimal investment strategy**:

$$
u^*(t) = - \frac{\frac{\partial W}{\partial F}}{F \frac{\partial^2 W}{\partial F^2}} \cdot \frac{\delta - r}{\sigma^2}
$$


---

### **Nonlinear Partial Differential Equation for $\( W(t, F) \)$**  

Substituting the optimal strategy into the **HJB equation**, we obtain the **nonlinear PDE**:

$$
\frac{\partial W}{\partial t} + \frac{\partial W}{\partial F} (r F + \pi(t)) - \frac{1}{2} \left( \frac{\delta - r}{\sigma} \right)^2 \frac{\left( \frac{\partial W}{\partial F} \right)^2}{\frac{\partial^2 W}{\partial F^2}} = 0
$$

with **boundary condition**:

$$
W(N, F) = U(F)
$$



---



