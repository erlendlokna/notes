
## *Time value of money*

Formula for future value given interest rate and T - years:
$$\boxed{FV_T = PV (1 + r)^T}$$
Compound frequency, n. "How many times paying per unit of time"
$$FV_T = PV (1 + \frac{r}{n})^{Tn}$$
As $n \rightarrow \infty$ compounding frequencies become infitesimal and compounding become continous. Defining $c=n/r$:
$$FV_T = PV[(1+\frac{1}{c})^c]^{rT}$$
Since: $$lim_{c\rightarrow\infty}(1 + \frac{1}{c})^c = e = 2.71828...$$
We get the continous formula: $$\boxed{FV_T=PV e^{rT}}$$ and we have $$ln \frac{FV_T}{PV} = ln e^{rT} = rT$$
* These logarithmic rates of return are used in continous time finance (option pricing)
* Advantages:
	* easily calculated from e.g daily stock prices $S_0, S_1$ etc
	* Additative over time:
		$$ln(\frac{S_1}{S_0}\frac{S_2}{S_1}) = ln(\frac{S_1}{S_0}) + ln(\frac{S_2}{S_1}) = ln(e^{r_1}) + ln(e^{r_2}) = r_1 + r_2$$
	* Not additative over investments.
		* Logartithmic transformation not linear
		* Log of sum $\neq$ sum of logs



### Annuities and Perpetuities 
* Cash flows (payments and receipts) often come in series
* called annuity (yearly) and perpetuity (for ever)
* Use mathematical series properties to calculate value

n-payments of ammount A:

$$PV = \frac{A}{1+r} + \frac{A}{(1+r)^2} + \cdots + \frac{A}{(1+r)^n}$$
Not frequently used in ninance. One exception: **Gordon growth model**
Present value of perpetuity (= annuity with infinite number of payments)
$$PV =\frac{A}{r}$$
with growth rate, g:
$$\boxed{PV = \frac{A}{r-g}}, r>g$$
(NB: typical exam question)


### Utility and risk aversion
* prefer A to B: $A \succ B$
* Prefer bundle 1 to 2: $B1 \succ B2$
* If A is preffered to B then utility of A, $U(A)$, is larger than utility of B, $U(B)$
$$A\succ B \iff U(A) > U(B) $$
Assumtions:
* Preferences can be expressed in utility functions
	* Assigns numerical values to a set of choices
* Utility function is concave
* Some well known utility functions (W: wealth):
	* Logarithmic utility function: $U(W) = ln(W)$. Requires W > 0
	* quadratic utility function: $U(W) = \alpha + \beta W - \gamma W^2$. Is only increasing over a certain range of W values. Bliss point: $W = 1/2 \beta / \gamma$
	* Not so well behaved.

**Two important concepts from utility functions:**
1. Indifferent curves:
	* combination of choises that give the same utility.
	* Instruments in rational decision making process
	* Their shape and location determine the economic choices
	* ’map’ all indifference curves on all possible choices and choose alternative  on highest indifference curve

2. Risk aversion:
	* risk is a negative quality, something to be avoided
	* (most) people require a reward to accept risk
	* floows from concave utility functions

Graphically the indifference curve is where the utility surface intersects fixed value plane.
* U(W) = 600 for example

**Risk aversion**
introduce a uncertainty for W. 
We can calculate two things:
1. $U(E[W])$ utility of expected wealth is on the utility function
2. $E[U(W)]$ expected utility of wealth is a straight line interpolation between points on the utility function.
![[utilityfunc.png]]

Example:
* $U(50) = 225$ & $U(150) = 525$
* $E[U(W)] = (225 + 525) / 2$ = 375
To how much certain W corresponds a utility of 375?
* doing the inverse of U for 375 we get $W=91.89$. Called *Certainty equivalent*
* Required risk premium: $100 - 91.89 = 8.11$

**Fisher's optimal investment analysis:**
* Investigates choice between investment and consumption over time
* Decisions made with indifference curves

Setting of fishers analysis:
