
### Practical application - investment analyses
Technology project ZXco. Accounting data:
![[exp1.png | 400]]

![[exp2.png | 400]]
Details:
* will generate sales in 3 years, 250, 500 and 250  
* sales start 1 year after investment  
*  50% work will be outsourced  
*  operating costs are 35, 65 and 30  
*  requires investment now of 180, plus 15 paid for test  
*  investment depreciated in equal parts: (180+15)/3=65  
*  required working capital 10 now and 20, 35 after 1,2 years  
*  working capital liquidated last year

-> Gives no clear decision criterion. Accept or not?

Could use their weighted averages:
$$\frac{205 \cdot 0.085 + 150 \cdot 0.56 + 100 \cdot0.21}{205 + 150 + 100} = 0.269 > CoC$$
CoC: Cost of capital

This ignores time & risk: later returns less valuable

**Financial representation** provides proper decision framework:
* Uses only data relevant for decision
* Uses cash flows as they occur, no arbitrary divisions over time

![[FinancialPOW.png | 400]]

$$NPV = \frac{72.5}{1.25} + \frac{134}{1.25^2} + \frac{121}{1.25^3} = 15.7$$
Decision rule:
* ZXco should go ahead with project if NPV > 0
* then project adds to the value of the company

Other investment criteria:
* Internal rate of return = discount rate that makes NPV = 0
$$-190 + \frac{72.5}{1+r} + \frac{134}{(1+r)^2} + \frac{121}{(1+r)^3} = 0$$
giving $r=0.3$
* Leads to correct decision if used with rule: invest if IRR > CoC

#### What does risk mean for our choice problems

There are many quantitative risk measures but :
Standard statistical measure of dispersion most often used: Variance or its square root standard deviation
$$\sigma, \sigma^2$$
Has some dissadvantages:
* Upward and downward deviation treated equally
* ignores higher moments (skewness, kurtosis)
* sometimes fails (e.g in case of stochastic dominance)

#### Calculating portfolio risk and return
Example:
|Scenario | 1| 2| 3|
|---|----|---|---|
|Probability $\pi$|1/3|1/3|1/3|
|return asset 1 $r_1$|.15|.09|.03|
|return asset 2 $r_2$|.06|.06|.12|

Expected asset return:
$$E[r_i] = \sum_{n=1}^N \pi_n r_{ni}$$
probability weighted sums over scenarios
$E[r_1] = 1/3 \cdot .15 + 1/3 \cdot .09 + 1/3 \cdot .03 = .09$

Asset variances:
$$\sigma_i^2 = \sum_{n=1}^N \pi_n(r_{ni} - E[r_i])^2$$
Expected portfolio return:
$$E[r_p] = \sum_{i=1}^lx_iE[r_i]$$
$x_i$: Asset weights. The sum of these is equal to 1

$$\sigma_p^2 = \sum_{n=1}^N \pi_n[x_1 r_{n1} + x_2 r_{n2} - (x_1 E[r_1] + x_2E[r_2])]^2$$

summation is over N scenarios. Rearanging terms:
$$\sigma_p^2 = \sum_{n=1}^N \pi_n[x_1(r_{n1} - E[r_1]) + x_2(r_{n2} - E[r_2])]^2$$
$$\sigma_p^2 = x_1^2\sigma_1^2 + x_2^2 \sigma_2^2 + 2x_1x_2\sigma_{1,2}$$
$$\sigma_{ij} = \sum_{n=1}^N \pi_n(r_{ni} - E[r_i])(r_{nj} - E[r_j])$$



**The contribution of each stock to portfolio risk**
Risk of individual asset is not its variance, but its contribution to portfolio risk. -> Covariance 

for stock 1 in a 2 stock portfolio:
$$contr_1 = x_1^2\sigma_1^2 + x_1x_2\sigma_{1,2}$$
$$= x_1[x_1cov(r_1, r_1) + x_2cov(r_1, r_2)]$$
Use full properties of covariance:
1. $cov (z_1, y ) + cov (z_2, y ) = cov (z_1 + z_2, y )$
2. $cov (c \cdot z, y ) = c \cdot cov (z, y )$

$$\implies contr_1 = x_1[cov(r_1, r_p)]$$
The relative contribution is the fraction:
$$\frac{contr_1}{\sigma_p^2} = \frac{x_1[cov(r_1, r_p)]}{\sigma_p^2} = x_1\frac{\sigma_{1,p}}{\sigma_p^2} = x_ 1\beta_1$$

$$\beta_i = \frac{\sigma_{i,p}}{\sigma_p^2}$$
$\beta_i$ measures systematic risk.
* $\beta_i$ > 1: change more than proportonally with change in portfolio returns
* $\beta_i$ < 1: change less than proportionally

Like variance $\beta_i$ is an objective measure.

$$\beta_p = \sum^i x_i\beta_i$$
$$\beta_{company} = x_1 \beta_{proj.1} + ... +x_n\beta_{proj.n}$$
$$\beta_{company} = x_E \beta_{equity} + x_D\beta_{depth}$$
**Correlation coefficient**
$$-1 \leq \mathbf{\rho_{ij}} = \frac{\sigma_{ij}}{\sigma_i \sigma_j} \leq 1$$
Gives: 
$$\sigma_p^2 = x_1^2\sigma_{1}^2 + x_2^2 \sigma_{2}^2 + 2x_1x_2\sigma_{1,2}$$
$$\sigma_{p}^2 = x_1^2\sigma_{1}^2 + x_2^2\sigma_{2}^2 + 2 x_1x_2\rho_{1,2}\sigma_{1}\sigma_{2}$$
Maximum diversification if $\rho$ is minimal (i.e -1)

Example:
- Take 4 stocks (1, 2, 3, 4) in future scenarios

![[exp11.png | 400]]
![[exp12.png]]

