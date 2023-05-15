## Fundamentals
>[!summary] Time value of money
> Formula for future value given interest rate(r) and years (T)
> $$\boxed{FV_T = PV (1 + r)^T}$$
> Compund frequency, n: How many times paying per unit of time
> $$FV_T = PV (1 + \frac{r}{n})^{Tn}$$
> continous formula: 
> $$\boxed{FV_T=PV e^{rT}}$$
> $$ln \frac{FV_T}{PV} = ln e^{rT} = rT$$
> Used in continous time finance (option pricing). They are additative over time
> $$ln(\frac{S_1}{S_0}\frac{S_2}{S_1}) = ln(\frac{S_1}{S_0}) + ln(\frac{S_2}{S_1}) = ln(e^{r_1}) + ln(e^{r_2}) = r_1 + r_2$$

>[!summary] Annuities and Perpetuities
> - Cash flows (payments and receipts) often come in series
>- called annuity (yearly) and perpetuity (for ever)
>- Use mathematical series properties to calculate value
>n - payments of ammount A:
>$$PV = \frac{A}{1+r} + \frac{A}{(1+r)^2} + \cdots + \frac{A}{(1+r)^n}$$
>**Gordon growth model** (Annuity with infinite number of payments)
>$$PV = \frac{A}{r}$$
>growth rate: g
>$$\boxed{PV = \frac{A}{r-g}}, r>g$$
>

>[!summary] Utility and risk aversion
>* prefer A to B: $A \succ B$
>* Prefer bundle 1 to 2: $B1 \succ B2$
>* If A is preffered to B then utility of A, $U(A)$, is larger than utility of B, $U(B)$
>$$A\succ B \iff U(A) > U(B) $$
>


## Modern Portfolio Theory
>[!summary] Portfolio Risk and Return
>
>Expected asset return: $\boxed{E[r_i] = \sum_{n=1}^N \pi_n r_{ni}}$
>Asset variance: $$\boxed{\sigma_i^2 = \sum_{n=1}^N \pi_n(r_{ni} - E[r_i])^2}$$
>Expected portfolio return: $$\boxed{E[r_p] = \sum_{i=1}^lx_iE[r_i]}$$
>Portfolio variance: $$\boxed{\sigma_p^2 = x_1^2\sigma_1^2 + x_2^2 \sigma_2^2 + 2x_1x_2\sigma_{1,2}} = \sigma_p^2 = x_1^2\sigma_1^2 + x_2^2 \sigma_2^2 + 2x_1x_2\rho_{1,2}\sigma_1\sigma_2 $$
> Contribution of each stock to portfolio risk:
> $$contr_1 = x_1[cov(r_1, r_p)] = x_1[x_1\sigma_1^2+x_2\sigma_{1,2}]$$
> $$\boxed{\frac{contr_1}{\sigma_p^2} = x_1 \beta_1}$$
> $$\beta_1 = \frac{\sigma_{i,p}}{\sigma_p^2}$$
> $\beta$ measures systematic risk (market risk / risk you cant reduce)
> $$\beta_p = \sum^i x_i\beta_i$$


>[!summary] capital market line 
>- equilibrium risk-return relation for efficient portfolios
>- only valid when all risk comes from share of market portfolio M in any portfolio p
>- Expression for CML: invest $x$ in M and $(1-x)$ risk free
>$$\boxed{E[r_p] = (1-x)r_f + xE[r_m]}$$
>$$\sigma_p = x\sigma_m$$
>$$x = \frac{\sigma_p}{\sigma_m}$$
>$$E[r_p] = r_f + \frac{E[r_m]-r_f}{\sigma_m}\sigma_p$$
>= timevalueofmoney + (price/unit risk) volume of risk


## CAPM and APT
Two asset portfolio
- One asset is market portfolio M, weight (1-x)
- The other asset is individual stock i, weight x
Risk return characteristics is:  $E[r_p] = xE[r_i] + (1-x)E[r_m]$

>[!summary] Capital asset pricing model: 
>$$\boxed{E[r_i] = r_f + (E[r_m] - r_f)\frac{\sigma_{i,m}}{\sigma_m^2}=E[r_i] = r_f + (E[r_m] - r_f)\beta_i}$$
>- clear price of risk:  $E[r_m] - r_f$
> - clear measure of risk: $\beta$
> - If asset i increases portf. risk $E[r_i]>E[r_p]$
> - Its graphical representation is known as security market line SML
> - Pricing relation for the entire investment universe
> 	- including inefficient portfolios
> 	- including individual assets

**1. Systematic and unsystematic risk**
- CML is pricing relation for efficient portfolios: $$E[r_p] = r_f +\frac{E[r_m]-r_f}{\sigma_m}\sigma_p$$
- SML becomes:$$E[r_p] = r_f + \frac{E[r_m]-r_f}{\sigma_m}\rho_{p,m}\sigma_p$$
- SML only prices systematic risk. Is therefore valid for all investment objects.
- CML prices all risks. Only valid when risk is systematic risk, ie for efficient portfolios. Otherwise CML uses 'wrong' risk measure
- if $\rho=1$ SML=CML


**2. CAPM and discount rates**
general valuation formula for investments: $value = \sum^t +\frac{Exp(cash flows)}{(1 + discount rate_t)^t}$

$$E[r_p] = r_f + (E[r_m]-r_f)\beta_p = \frac{E[V_{p,T}-V_{p,0}]}{V_{p.0}}$$
$$\implies \boxed{V_{p,0}= \frac{E[V_{p, T}]}{1+r_f+(E[r_m]-r_f)\beta_p}}$$
$r_f$ is the time value of money. Equation for risk adjusted discount rate

**3. Certainty equivalent formulation of CAPM**
$$\boxed{V_{p,0} = \frac{E[V_{p,t}]-\lambda cov(V_{p,T}, r_m)}{1+r_f}}$$
market price of risk: $\lambda = \frac{E[r_m]-r_f}{\sigma_m^2}$

**4. Performance measures Portfolio management involves trafe-off**
>[!tip] **Sharpe ratio**
>$$SR_p = \frac{\bar{r_p} - \bar{r_f}}{\hat\sigma_p}$$
>- $\bar r_p$: is portfolio's historical average return $\bar r_p = \sum_t r_{pt}/T$
>- $r_f$ is historical average risk free interest rate
>- $\hat \sigma_p$ is stand.dev. portf. returns. $\hat \sigma_p = \sqrt{\sum_t(r_{pt}-\bar r_p)^2 / T}$
> 
> Widely used to:
>- Can be used to rank portfolios, funds or managers
>- Identify poorly diversified portfolios (too high $\hat \sigma_p$)
>- identify funds that charged too high fees ($\bar r_p$ too low)

>[!tip] Treynor ratio
>uses security market line, $\beta$ as risk measure:
>$$TR_p = \frac{\bar r_p - \bar r_f}{\hat B_p}$$
>$\hat B_p$ is estimated using historican returns
>- All assetts lie on SML $\implies$ all have same TR

>[!tip] Jensen's alpha
>also based on CAPM. Measures portfolio return in excess of CAPM
>$$\hat \alpha_p = \bar r_f - (\bar r_f + \hat B_p)$$

>[!summary] Comparison
>- Sharpe ratio uses total risk ($\sigma_p$)
>- Treynor ratio and jensen's alpha take only systematic risk $\beta$ into account
>- Sharpe is better for evaluating investor's total portfolio
>- When portfolios is split up into subportfolios sharpe will ignore correlations and overstate risk
>- Treynor is more appropriate for well-diversified subportfolios

**Single Index Model**$$\boxed{r_i = \alpha_i + \beta_i r_m + \epsilon_i}$$
- Assumes there is only 1 reason why stocks covary: they all respond to changes in market as a whole
	- Stocks respond in different degrees (measured by $\beta$)
	- Stocks do not respond to unsystematic (not marked related) changes in other stocks values
- $\alpha_i$ : expected return not related to the return of the marked
- $\beta_ir_m$ : return that is related to the return of the market. Systematic risk
- $\epsilon$ : random element. Unsystematic risk

Two assumptions:
* $cov(r_m, \epsilon_i)=0$ : random element of non marked related return not correlated with market return
* $cov(\epsilon_i, \epsilon_j)=0$ for all $i\ne j$ : random elements of non marked related returns are uncorrelated

	$\sigma_i = \beta_i^2 \sigma_m^2 + \sigma_{\epsilon i}^2$  $\sigma_{i,j}=\beta_i \beta_j \sigma_m^2$

Expression for multiple stock returns become:
$$r_i = \alpha_i + b_{1, i} F_1 + b_{2, i}F_2 +\dots + b_{K,i}F_k$$
- $b_{1,i}$ sensitivity of stock i for changes in factor $F_1$
- $F_1$ = return on factor 1, etc

**Arbitrage Pricing Theory, APT**
Arbitrage = The practise of exploiting price differences between two or more markets to make profic
$$\boxed{r_i = E[r_i] + \sum_{k=1}^Kb_{ik}(F_k-E[F_k])+\epsilon_i}$$
- $E[r_i] =$ expected return of stock i
- $b_{ik}=$ sensitivity of stock i to factor k
- $F_k=$ return of factor k, with $E[F_k-E[F_k]]=0$. Fair game
- $\epsilon_i=$idiosyncrativ return stock i. $E[\epsilon]=0$

Next, construct portfolio, I assets, weights $x_i$, then portfolio return is:
$$r_p = \sum_{i=1}^Ix_ir_i=\sum^I_{i=1}x_iE[r_i]+\sum^I_{i=1}\sum_{k=1}^Kx_ib_{ik}(F_k-E[F_k]) + \sum^I_{i=1}x_i\epsilon_i$$
In well diversified portfolios, idiosyncratic risk(last term) disapears. $\sum_{i=1}^I x_i\epsilon_i = 0$

APT's equilibrium condition is: *The absence of arbitrage opportunities*


## Market efficiency
**Efficiency concept**
A market in which prices always fully reflect available information is called efficient

$$\epsilon_{i, t+1}=r_{i,t+1}-E[r_{i,t+1}| \phi_t]$$
1. **Fair game model**: $E[\epsilon_{i, t+1}|\phi_t]=0$
	- $\phi_t$ cannot be used to systematically earn excess returns 
2. **Martingale model**: $\epsilon_t > 0$, $E[\epsilon_{i, t+1}|\phi_t]=0$
	$\implies P_0 = \frac{E[P_t]}{(1+r)^t}$
	- properly discounted expected future value = present value
	- Dynamic process with that process is called martingale
	- No info in $\phi_t$ improves forecast of $E[P_{i,t}|\phi_t]$ beyond $P_{i,t}$
3. **Random walk model**: Fair game and maringale model only consider expectation
	- Excess returns follow random walk. Constant (called drift)
	- Excess returns has zero expectations. iid in all future periods

**Empirical implications**
1. **No autocorrelation in (excess-)returns**
	- autocorr = corr with itself 1 or more periods ago $corr(r_t, t_{t-x}), x=1,2,...$
	- EMH implies return 1,2, .. periods ago says nothing about return of this period
2. **Investment strategies give no positive excess returns**
	- If markets are efficient, all strategies fail to consistently produce positive excess strategies
3. **Investment funds and (groups of) investors do not systematically differ in excess returns**
	- If markets are efficient, no fund can systematically earn positive excess returns 
4. **Prices adjust to new information in an efficient way**
	- quickly and unbiased. No under or overcorrelation

## Capital structure
**Common stocks (or shares)**: 
- permanent investments, profit dependent return, ownership
- low priority (residual claim), no upper limit
- usually deposited, can be stock market traded
- unsecured, can be underlying for derivatives
**Bonds and bank loans** : 
- Temperorary investments, predetermined return, no property rights
- high priority, fixed maximum return
- deposited, bonds can be stock market traded
- can be secured, bonds can be underlying for derivatives

Many types of bonds:
* *ordinary bonds* (corporate or government)
* *income bonds*: only pay interest if profit allow it
* *index bonds*: interest dependent on government bonds or something else eg. price of railway tickets
...

Depth can be secured with:
- Priority claims on certain assets:
	- mortage, inventories, accounts receivable, also assets outside the firm (private house or jewellery)
	- 