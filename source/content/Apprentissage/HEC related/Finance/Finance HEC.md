---
tags:
  - finance
  - études/finance
---
###### Best Finance Movies
- Wall Street (1987) 78% rotten tomatoes
- Inside Job (2010) 98% rotten tomatoes
- Margin Call (2011) 88% rotten tomatoes
- The Wolf of Wall Street (2013) 78% rotten tomatoes
- The Big Short (2015) 88% rotten tomatoes
----
#### Sommaire
- [[S&P 500]]
- [[Passive VS Actif management]]
- [[type of investment]]


# Basic Finance
Une seul question: **Combien d'argent cela représente ?**
Puis, il faut **comparer ce montant** ou bien lui donner un ordre d'idée. Car, 1$ aujourd'hui vaut plus qu'1$ dans 100ans. Et prendre en compte la taxation !!!

Ainsi, on peut rajouter 2 unités au signe $:
 - Taxes retirée 
	 - 1000$ au black > 1000$ supplémentaire de revenus d'emploi
 - $ selon quel année
	 - On parle de $ reçu dans le présent, passé, futur ? 


## Formules Financières


###### Valeur actuel 
**Valeur actuelle d’un flux de trésorerie** :
$$PV = \frac{FV}{(1 + r)^t}$$

**Valeur actuelle d’une perpétuité** :
$$PV = \frac{C}{r}$$
**Valeur actuelle d’une annuité** :
$$PVA = C \times \left[ \frac{1 - (1 + r)^{-t}}{r} \right]$$

**Valeur future d’une annuité** :
$$FVA = C \times \left[ \frac{(1 + r)^t - 1}{r} \right]$$

**Valeur actuelle d’une perpétuité croissante** :
$$PV = \frac{C}{r - g}$$


##### Prix des actifs

**Prix d’une obligation** :
$$P_0 = C \times \left[ \frac{1 - (1 + r)^{-t}}{r} \right] + \frac{FV}{(1 + r)^t}$$

**Prix d’une action avec dividende constant (sans croissance)** :
$$P_0 = \frac{D_1}{k}$$

**Prix d’une action avec dividende croissant** :
$$P_0 = \frac{D_1}{k - g}$$


##### Present value of the capital cost depreciation tax shield according to the declining balance method, and present value of tax shield lost
$$PVCCATS = \left[ \frac{C \cdot d \cdot \tau}{r + d} \right] \times \left[ \frac{1 + 0.5r}{1 + r} \right]$$

$$PV(TSL)_{salvage} = \left[ \frac{S \cdot d \cdot \tau}{r + d} \right] \times \left[ \frac{1}{(1 + r)^t} \right]$$

##### Present value of the capital cost depreciation tax shield according to the straight-line method
$$VSLTS = \left[ \frac{C \cdot \tau}{v} \right] \times \left[ \frac{1 - \frac{1}{(1 + r)^t}}{r} \right]$$

#### CAPM et rendement
**Rendement attendu d’un titre** 
$$E(R) = \sum_{i=1}^{n} P_i \cdot R_i$$
###### Variance du rendement
$$\text{Var}(R) = \sum_{i=1}^{n} P_i \cdot (R_i - E(R))^2$$

**Rendement attendu d’un portefeuille à deux actifs** :
$$E(R_p) = xE(R_A) + (1 - x)E(R_B)$$

**Variance d’un portefeuille** :
$$\text{Var}(R_p) = x^2\text{Var}(R_A) + (1 - x)^2\text{Var}(R_B) + 2x(1 - x)\text{Cov}(R_A, R_B)$$

**Corrélation entre les actifs A et B** :
$$\text{Corr}(R_A, R_B) = \frac{\text{Cov}(R_A, R_B)}{\sqrt{\text{Var}(R_A)} \sqrt{\text{Var}(R_B)}}$$
**Modèle CAPM** :
$$E(R_i) = R_f + \beta_i(E(R_M) - R_f)$$

**Bêta** :
$$\beta_i = \frac{\text{Cov}(R_i, R_M)}{\text{Var}(R_M)}$$

#### Cout du capital
**Coût des fonds propres (modèle de croissance des dividendes)** :
$$R_E = \frac{D_1}{P_0} + g$$


**Coût des actions privilégiées** :
$$R_P = \frac{D_1}{P_0}$$


**Coût moyen pondéré du capital (WACC)** :
$$WACC = \frac{E}{V}R_E + \frac{D}{V}R_D(1 - T_C)$$

**Weighted average issuance costs**
$$f_A = \frac{E}{V}f_E + \frac{D}{V}f_D$$






# Fundamental Concepts of Finance
#### Risk 
- Dead cat bounce
- Risk aversion
- Market efficiency

#### Interest rate
###### Tips : 

>Always make sure that the interest rate and the time period match.  

E.g., if the APR is 12% with monthly compounding, the semiannual rate is not 6%. You would need an APR based on semiannual compounding to find the semiannual rate.


###### Definition
**Real rate of interest** – Interest rates or rates of return that have been adjusted for inflation. We are concerned not with the number of dollars we will have, but with how much those dollars will buy.

**Nominal rate of interest** – Interest rates or rates of return that have not been adjusted for inflation.

*The important thing to remember is to match real cash flows with real rates and nominal cash flows with nominal ones.*

#### Loan
There are three basic types of loans

**Pure Discount Loans:** The borrower receives money today and repays a single lump sum at some time in the future. Treasury bills are a good example: The principal amount is repaid at some future date, without any periodic interest payments.

**Interest-Only Loans:** The borrower pays interest each period and repays the entire principal at some point in the future. The cash flow stream is similar to the one of a corporate bond.

**Amortized Loans**: The borrower is required to repay parts of the principal amount over time. The process of making regular payments to reduce the principle is called amortizing the loan

#### Bond
A **bond** is a debt security that is typically issued by a corporation or government to obtain long-term financing. To repay the money, the borrower agrees to make specific interest and principal payments on pre-specified dates.

The **basic terms of a bond** issue include

- **Coupon payments**: Regular (interest) payments made to the bond holder, typically semi-annually. Can be expressed in the coupon-rate as a percentage of the face value. The coupon rate is an APR.
- **Face value (par value)**: Principal amount to be repaid at maturity. The face value of most corporate bonds is $1,000. The face value for government bonds is generally much higher.
- **Maturity date**: The date when the principal amount is due and interest payments stop. The time until this date is the time to maturity (TTM).
- The total amount of bonds issued.

![[BondsValuation.png]]

###### Classes of Issues
**Treasury debt (Federal Government):**
- Bills: (zero coupon), maturity 1 year or less
- Notes: coupons paid twice/year, maturity 2 to 10 years
- Bonds: coupons paid twice/year, maturity greater than 10 years

**Corporate bonds**

**Agency issues**
- Fannie Mae, and Freddie Mac
- Municipal Bonds (tax benefits)
- States (e.g., Florida)
- Cities (e.g., New York City)


##### Yield to Maturity
The **Yield to Maturity (YTM)** is the discount rate that equates the present value of a bond’s future cash flows with its current price. It represents the total annual return the purchaser would receive if the bond were held to maturity.

As the current price is determined by market participants, the YTM reflects the market’s opinion of what the appropriate discount rate is.

The YTM is a more convenient indicator of a bond’s attractiveness than its price
- A **discount bond** is a bond that sells for less than its face value. This is the case whenever YTM > Coupon rate.
- A **premium bond** is a bond that sells for more than its face value. This is the case whenever YTM < Coupon rate.
- A bond that sells for exactly its face value is said to sell **at par**. This is the case whenever YTM = Coupon rate.

![[StructureInterestRate.png]]

##### Debt v Equity
**Debt**: 
- Not an ownership interest
- Bondholders do not have voting rights
- Interest is considered a cost of doing business and is tax deductible
- Bondholders have legal recourse if interest or principal payments are missed
- Excess debt can lead to financial distress and bankruptcy

**Equity:**
- Ownership interest
- Common shareholders vote for the board of directors and other issues
- Dividends are not considered a cost of doing business and are not tax deductible
- Dividends are not a liability of the firm and shareholders have no legal recourse if dividends are not paid
- An all-equity firm can not go bankrupt



### Time value of money: 
**is $1 the same as $1 next year?**
- Time premium (people are impatient)
- Inflation premium (prices rise, on average)

> A dollar earned today is worth more than a dollar earned tomorrow.

###### Vocabulary
1. Present Value (PV)  – earlier money on a timeline
2. Future Value (FV)  – later money on a timeline
3. Interest rate  – the “price” of time
4. Compounding  – translating earlier money to later money
5. Discounting  – translating later money to earlier money


Formula :  ==PV = FVt / (1+r)^t==

### Uncertainty:
**how much is $1 worth that is invested in a project that may pay $2 or $0 next year?**

•Risk premium (we want to be incentivized to take on risk)


### Value of an asset
![[valueAsset.png]]