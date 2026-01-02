# One-Period-Binomial-Model
**One-Period Binomial Option Pricing Model and Arbitrage Detection**

**MotiVation and Learning Objectives**
Master the fundamental principle of replication in complete markets. Understand how absence of arbitrage forces unique pricing, and establish foundations for risk-neutral valuation thatextends to continuous-time models.
**Key Skills:** Replication, arbitrage detection, state pricing, delta hedging, market completeness.

**Comprehensive Mathematical Development**
Let (Ω,F,P) be a probability space with two states: $\omega_u$ (up) and $\omega_d$ (down). The underlying asset price evolves as:


S1(ω) =


      {Su = S0u if ω = $\alpha$


      {Sd = S0d if ω = $\omega_c$


where u > 1 and 0 < d < 1 are deterministic multipliers.


A riskless bond evolves as B0 = 1, B1 = 1 + r with r > −1.


**Theorem 1 (No-Arbitrage Condition)**: The market is arbitrage-free if and only if:

                                        0 < d < 1 + r < u


**Proof**. If 1 + r ≤ d, the bond is dominated by the stock in all states, creating arbitrage by shorting the bond and buying the stock. Conversely, if u ≤ 1+r, the stock is dominated. When d < 1 + r < u, the law of one price holds and replication is possible.


**State Price Density:** Under no-arbitrage, there exist unique risk-neutral probabilities:
q =((1 + r) − d)/(u − d), 
1 − q = (u − (1 + r))/u − d


**Option Pricing:** For a contingent claim with payoffs Cu, Cd, the arbitrage-free price is:
C0 = (1/1 + r)*EQ[C1] = qCu + (1 − q)Cd/1 + r


**Replication Strategy:** Construct portfolio (Δ, B) where:


Δ =Cu − Cd/S0(u − d)  **(shares)**

B = uCd − dCu/(u − d)(1 + r)  **(bond position)**

The portfolio value V1 = ΔS1 + B(1 + r) replicates the claim in both states.


**Greeks in Binomial Model:**

Δ = ∂C0/∂S0 = (Cu − Cd)/(S0(u − d))


Γ ≈ (Δu − Δd)/(S0(u − d)/2)
