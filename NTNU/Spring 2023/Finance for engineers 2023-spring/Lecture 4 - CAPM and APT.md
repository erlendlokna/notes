**CAPM** is a more general model. 
Consider two asset portfolio
- One asset is market porfolio M, weight (1-x)
- other is individual stock i, weight x

$$E[r_p] = xE[r_i] + (1-x)E[r_m]$$
$$\partial_x E[r_p] = E[r_i] - E[r_m]$$

$$\partial_x \sigma_p = \frac{x(\sigma_i^2 + \sigma_m^2 - 2\sigma_{i,m}) + \sigma_{i,m}-\sigma_m^2}{\sigma_p}$$
at point M all funds are invested in M so that 
- x = 0, $\sigma_p = \sigma_m$
- in equilibrium M excess demand is zero
This simplifies marginal risk to:
$$\partial_x\sigma_p|_{x=0} = \frac{\sigma_{i,m} - \sigma_{m}^2}{\sigma_p}=\frac{\sigma_{i,m} - \sigma_{m}^2}{\sigma_m}$$

the slope of the risk-return trade off at equilibrium point M is:
$$\frac{\partial_x E[r_p]}{\partial_x\sigma_p}|_{x=0} = \frac{E[r_i]-E[r_m]}{(\sigma_{i,m}-\sigma_m^2) / \sigma_m}$$
at point M the slope of the risk-return trade off is also the slope of CML:

$$\frac{E[r_i]-E[r_m]}{(\sigma_{i,m}-\sigma_m^2) / \sigma_m} = \frac{E[r_m]-r_f}{\sigma_m}$$
$$\implies \boxed{E[r_i]=r_f + (E[r_m]-r_f)\frac{\sigma_{i,m}}{\sigma_m^2} = r_f + (E[r_m]-r_f)\beta_i}$$
**=Capital Asset Pricing model (CAPM)**
- The graphical representation is known as the Security Market Line
- Clear price of risk: $E[r_m]-r_f$
- Clear measure of risk: $\beta$
- Well-diversified investors value assets according to their contribution to portfolio risk
	- if asset i increases portf. risk $E[r_i] > E[r_p]$
	- if asset i decreases portf.risk $E[r_i] < E[r_p]$
- Expected risk premium prop to $\beta$

Four insights offered by the model:
1. Systematic and unsystematic risk
2. risk adjusted discount rates
3. Certainty equivalents
4. Performance measures

#### 1. Systematic & unsystematic risk

- The CML is pricing relation for efficient porfolios
- $\frac{E[r_m]-r_f}{\sigma_m}$ is the price per unit of risk
- $\sigma_p$ is the volume of risk

The SML valid for all investments, incl inefficient portfolios and individual stocks:
$$E[r_p] = r_f + (E[r_m]-r_f)\beta_p$$
$$\beta_p = \frac{cov_{p,m}}{\sigma_m^2} = \frac{\sigma_p\sigma_m\rho_{p,m}}{\sigma_m^2} = \frac{\sigma_p\rho_{p,m}}{\sigma_m}$$
$$E[r_p] = r_f + \frac{E[r_m] - r_f}{\sigma_m}\sigma_p\rho_{p,m}$$
- The difference between CML and SML is in volume part:
- SML only prices the systematic risk
- CML prices all risks 
	- Only valid when all risk is systematic risks, i.e for efficient portfolios
	- otherwise, CML uses 'wrong' risk measure

- Difference is correlation term, that is ignored in CML
- if $\rho_{p,m}=1 \implies \sigma_m\rho_{p,m}=\sigma_p$ and CML = SML

#### 2. CAPM and discount rates
General valuation formula for investments:
$$Value = \sum^T\frac{Exp[Cash flows_t]}{(1+discount rate_t)^t}$$
CAPM gives expected return of portfolio P as:
$$E[r_p] = r_f + (E[r_m]-r_f)\beta_p$$
Also as:
$$E[r_p] = \frac{E[V_{p,T}] - V_{p,0}}{V_{p,0}}$$
- Links expected end-of-period value, $E[V_{p,T}]$ to value now, $V_{p,0}$
- found by equation the two expressions:
$$\frac{E[V_{p,T}] - V_{p,0}}{V_{p,0}} = r_f + (E[r_m]-r_f)\beta_p$$
$$\boxed{V_{p,0} = \frac{E[V_{p,T}]}{1+r_f+(E[r_m]-r_f)\beta_p}}$$
- $r_f$ is the time value of money
- $(E[r_m]-r_f)\beta_p$ is the adjustedment for risk
- togheter they form the risk adjusted discount rate


#### 3. Certainty equivalent formulation
The second way to account for risk
- Adjust uncertain cash flow to a certainty equivalent
- can (or should) be discounted with risk free rate

$\beta_p = cov_{r_p, r_m}/\sigma_m^2$
$r_p = \frac{V_{p,t} - V_{p,0}}{V_{p,0}} = \frac{V_{p,t}}{V_{p,0}} - 1$

$$\implies V_{p,0} = \frac{E[V_{p,T}] - \lambda cov(V_{p,T}, r_m)}{1+r_f}$$

$$\lambda = \frac{E[r_m]-r_f}{\sigma_m^2}$$
= The certainty equivalent formulation of CAPM

#### 4. Performance measures Portfolio management involves a trade off

Uses the slope of CML for this:
$$E[r_p] = r_f +\frac{E[r_m] - r_f}{\sigma_m}\sigma_p\implies \frac{E[r_p]-r_f}{\sigma_p} = \frac{E[r_m]-r_f}{\sigma_m}$$
left hand side is return-to-variability ratio or **Sharpe ratio

$$\boxed{SR_p = \frac{\bar{r_p}-\bar{r_f]}}{\hat{\sigma_p}}}$$
- $SR_p$ is the sharpe ratio
- $\bar{r_p}$ is the porfolio's historical average return
- $\bar{r_f}$ is the historical average risk free interest rate
- $\hat{\sigma_p}$ is stand. dev portf. returns

**Used to:**
- rank portfolios, funds or managers
- identify poorly diversified portfolios (too high $\sigma_p$)
- identify funds that charged too high fees ($\bar{r_p}$ too low)


**Treynor ratio**
uses security market line, $\beta$, as risk measure:
$$\boxed{TR_p = \frac{\bar{r_p} - \bar{r_f}}{\hat{B_p}}}$$
$\hat{B_p}$ is estimated from historical returns

- Treynor ratio usually compared with risk premium market portfolio
- Usually compared with risk premium market portfolio
All assets lie om SML $\implies$ all have same TR

**Jensen's alpha**
also based on CAPM
- measures portfolio return in excess of CAPM
- found by regressing portfolio risk-premium on market portfolio's risk-premium
$$r_{pt}-r_{ft} = \hat{\alpha_p} + \hat{B_p}(r_{mt}-r_{ft}) + \hat{\epsilon_{pt}}$$
- taking averages and re-writing gives jensen's alpha:
$$\hat{\alpha_p} = \bar{r_p} - (\bar{r_f} +\hat{B_p}(\bar{r_m}-\bar{r_f}))$$

**Comparing performance measures:**
- Sharpe ratio uses total risk $\sigma_p$
- Treynor ratio and jensens alpha take only systematic risk $\beta$ into account

Sharpe ratio is better for evaluating investor's total portfolio
- When a portfolio is split into subportfolios Sharpe ratio will ignore correlations and overstate risk
- Treynor ratio is more appropriate for well-diversified subportfolios
Treynor and jensens alpha is dependent on the choice of market index or portfolio


**Assumptions CAPM is based on**
- Financial markets are perfect and competitive:
	- No taxes or transactional costs
	- large number of buyers and sellers
- ...

Key assumption is:
	Investors maximize expected utility of their end wealth by choosing investments based on their mean-variance characteristics
