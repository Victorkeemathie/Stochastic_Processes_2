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

To address these risks, actuaries rely on:
- **Geometric Brownian Motion (GBM)** – Investment returns.
- **Vasicek Model** – Interest rate dynamics.
- **Cox-Ingersoll-Ross (CIR) Model** – Stochastic interest rates.
- **Lee-Carter Model** – Mortality forecasting.
- **Cairns-Blake-Dowd (CBD) Model** – Longevity risk.
- **Vector Auto Regression (VAR)** – Economic dependencies.

---

## **2. Stochastic Models in Pension Pricing**

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

### **2.4 Lee-Carter Model – Mortality Rate Forecasting**
#### **Why is it used?**
Pension funds **pay out benefits until retirees pass away**. The **Lee-Carter model** forecasts **mortality rates** based on historical trends.

#### **Formula:**
$$
\ln m_x(t) = a_x + b_x k_t + \epsilon_{x,t}
$$

Where:
- $\( m_x(t) \)$ = Mortality rate at age $\( x \)$.
- $\( a_x \)$ = Average log mortality for age $\( x \)$.
- $\( b_x \)$ = Sensitivity of age $\( x \)$ to mortality trends.
- $\( k_t \)$ = Stochastic trend in mortality rates.

#### **How It Relates to Pension Pricing:**
- Helps estimate **life expectancy**, which determines **pension payouts**.
- Used to price **annuities and pension liabilities**.

---

### **2.5 Cairns-Blake-Dowd (CBD) Model – Longevity Risk**
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

### **2.6 Vector Auto Regression (VAR) – Economic Dependencies**
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

## **3. Conclusion**
Stochastic models provide actuaries with powerful tools to **price pensions accurately** by **accounting for uncertainty**. By integrating these models, actuaries can ensure **pension funds remain solvent in the long run**.
