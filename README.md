# CMS Cliquet

A CMS cliquet option has two legs: One leg of this deal is based on (regular) floating rates. The other leg links to CMS swap rates. Due to the “set-in-arrear” feature in the structured leg, convexity and timing adjustments have to be considered. See https://finpricing.com/lib/EqCliquet.html

Due to the embedded option and convexity adjustments in the structure leg, we need swap rate volatilities and forward rate volatilities. The former can be interpolated from the implied swaption volatility surface. The latter should be interpolated from the so-called implied forward volatility surface. 

However, this surface is currently not available in the market. Therefore, the swap rate volatility surface is also applied to forward rate volatilities.  The convexity adjustment does not explicitly depend on the correlation coefficient between the swap rate and the forward rate. 

Consider a fixed income contract consisting of a regular floating leg and a structured floating leg. 

Pricing the second leg of the contract is a little bit more involved. Firstly, there is an optionality which is embedded in the contract, and secondly, this leg does not incorporated a natural time lag, which implies that the convexity adjustment is needed.

Let Rcms(t; s) be a forward Δ-term CMS swap rate seen at time t and matured at time s. Clearly, Rcms(si) = Rcms (si; si). Here we have assumed that the underlying CMS swap structure, which includes the swap term (i.e., ¢), swap frequency f, day-count-basis, day-rollover-basis, and holiday-centre, has been specified and given. For each i = 1,…,N2, let Bi be the price at time si of a bond with the same structure of the CMS swap and the coupon rate being the initial forward CMS swap rate Rcms (tv; si), and yi be the yield of the bond

Now let V2 be the value of this leg and df(2) be the discounting factor from the time s back to the valuation date. Then the total payoff of this leg is given. Let E be the expectation operator under the risk-neutral world with respect to the discount bond matured at s. Thus the present value of this leg can be given.

If we can calculate the expectation of the future CMS swap rate, then present value (7) can be obtained by using Black’s formula. Considering the convexity adjustment, we can approximate the expectation.

