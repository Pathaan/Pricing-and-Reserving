# Pricing-and-Reserving
# Question

A life insurance company is planning to launch a new **without-profit endowment assurance product**. This product will be offered to all male and female individuals with the following boundary parameters:

* **Minimum age at entry:** 25 years
* **Maximum age at entry:** 40 years
* **Minimum Sum Assured:** 50,000
* **Maximum Sum Assured:** 5,00,000
* **Minimum Maturity Age:** 35 years
* **Maximum Maturity Age:** 50 years
* **Premium Payment Term:** Policy term less five years

The product is proposed to have the following features:

1. **Death benefit:**
   A death benefit equal to the **Sum Assured chosen by the policyholder** will be payable on the death of the policyholder during the **premium payment term**.

2. **Survival benefit:**
   A survival benefit equal to **10% of the Sum Assured** will be paid to the policyholder on surviving till the **end of the premium payment term**.

3. **Death after the premium payment term:**
   On death after the premium payment term but before the end of the policy term, the death benefit will be equal to the **original Sum Assured less the survival benefits already paid up to the date of death**.

The following basis is used while **pricing and profit testing** this product:

### Mortality

* **Male non-smokers:**
  Male non-smokers are expected to experience mortality in line with the **IALM 2012–14 table**.

* **Female non-smokers:**
  Female non-smokers are expected to experience **male non-smoker mortality with a 20% discount**.

* **Smokers:**
  Smokers are expected to experience the respective **male/female non-smoker mortality rates with a 40% premium**.

### Lapses

| Policy Year | Lapse Rate |
| ----------- | ---------: |
| 1           |        20% |
| 2–5         |        15% |
| 6–15        |        12% |
| 16 onward   |        10% |

## Expenses

### Initial Expenses

| Expense Type     |         Amount |
| ---------------- | -------------: |
| Fixed            | 250 per policy |
| % of Premium     |            15% |
| % of Sum Assured |          0.01% |

### Renewal Expenses

| Expense Type |                                                          Amount |
| ------------ | --------------------------------------------------------------: |
| Fixed        | 25 per policy per annum, incurred at the beginning of each year |
| % of Premium |                                                            1.5% |

| Event Based Expenses |  |
| --- | --- |
| Death Claim | 400 per policy |
| Maturity Claim | 200 per policy |
| Surrender Claim | 150 per policy |
| Survival Claim | 50 per policy |

Expense Inflation: Fixed renewal expenses will be inflated each year by 2.5% per annum

* Interest Rate: 8.25% per annum

*Set up a dynamic cashflow model which can be used for any model point in the Model Point table below by simply changing the model point number in the model. This model should be able to:*

* *Determine the premium for all the ten model points assuming i.) mortality as the only decrement ii.) no reserves are held iii.) profit margin of 4% for each policy*
* *Determine the Gross Premium Prospective Reserves at the end of each policy year for the 5ᵗʰ model point using the same premium and basis.*
* *Calculate the retrospective reserves using the same premium and basis for the 7ᵗʰ model point.*
* *Using the same premiums as those derived above and assuming no reserves are held, determine the profit margin assuming lapses as those given in the basis above and surrender value equal to the below*











* **Determine the premium for all the ten model points assuming i.) mortality as the only decrement ii.) no reserves are held iii.) profit margin of 4% for each policy?**

**Methodology of Pricing Products**

Based on Profit Targeting: Insurers asume a level of profitability and back-calculate the premiums to be charged to achieve that profitability.

Based on Competition: Products are highly competitive and price sensitive. They have to be constantly repriced in light of emerging new competition.


### Initial Expenses = Fixed Expenses + (Premium * % of Premium) + (Sum Assured * % of Sum Asured)

Note: Initial Expenses are incurred in the 1st Year only.


### Renewal Expenses:
If the policy year is blank, it will remain blank. Else we add the fixed and variable part of renewal expenses. Please note that the fixed expense part is inflated at the inflation rate.


### ALT + M + V for Evaluating formula 

### Interest = Interest *Net Cashflow
### Mortality: Calculated using the IAML table adjusted for the mortality factor depending upon the gender and smoking status of the Policyholder.
### Survival Probability: 1 - Mortality
### Survival Benefit:

It is payable only if the policyholder survives upto the Premium payment term.

According to the case study, the benefit payable is 10% of the sum assured. It will only be paid at the end of the year where the premium payment term ends, which is the tenth year in this case. The Sum assured is 1,50,000 that is why the survival benefit comes out to be 15,000

### Maturity Benefit:

Policy holder receives this only if he/she is alive at the end of the policy term.

The benefit payable is 50% of the sum assured at the end of the policy term. We can see that the maturity benefit comes out to be 75,000 which is 50% of 150,000.

### Survival Claim Expense:
Survival Expense * (1 + Expense Inflation) ^ (Policy Year - 1)

### Death Claim Expense:
Death Expense * (1 + Expense Inflation) ^ (Policy Year - 1)

### Maturity Claim Expense:
Maturity Expense * (1 + Expense Inflation) ^ (Policy Year - 1)

Note: This happens at end of the policy term.

### Expected Survival Cost:
(Survival Benefit + Survival Claim Expense) * Survival Probability

**Survival Claim Expense** should be incurred only in the year when Survival Benefit is paid which is when the Premium Payment Term ends. For Maturity Expense as well we need to make sure this is incurred only at the end of the policy term.

**Expected Death Cost** = (Death Benefit + Death Claim Expense) * Mortality Rate

**Expected Maturity Cost** = (Maturity Benefit + Maturity Claim Expense) * Survival Benefit

**Expected Net Cashflow/ Profit** = Premium - Initial Expenses - Renewal Expenses + Interest - Expected Survival Cost - Expected Death Cost - Expected Maturity Cost.

**Probability of staying in-force at the start of the first year** is 1.

**Probability of staying in-force at the start of the nth year** = Probability of staying in-force at the start of the (n-1)th year × Probability of surviving the (n-1)th year

**NPV of Profit for the model** = Sum of all the expected NPV for profit figures in column V

**Profit Signature** = Probability of staying in-force at the start of the year * Profit

**Discount Factor** = (1+Interest Rate)^(-n)
**Expected Present Value of Profit** = Profit Signature * Discount Factor


* **Determine the Gross Premium Prospective Reserves at the end of each policy year for the 5ᵗʰ model point using the same premium and basis.**
  
<img width="1432" height="733" alt="image" src="https://github.com/user-attachments/assets/b3bbade8-b8af-449d-9ca7-0d0c79d52d0b" />

**Prospective Reserve at Start of Year** = - Expected Net Cashflow / (1 + Interest Rate)

**Prospective Reserve at Start of the Current Year** = - Expected Net Cashflow at the End of the Current Year / (1 + Interest Rate) + Prospective Reserve at Start of Next Year * Probability of Survival in the Current Year

In other words, **the reserves at the start of the 9th year** = Expected net cashflow at the end of the 9th year discounted for one year and expected net cashflows at the end of the 10th year discounted back for two years and multiplied by the probability of survival in the 9th year.

**Calculate the retrospective reserves using the same premium and basis for the 7ᵗʰ model point.**

<img width="2199" height="639" alt="image" src="https://github.com/user-attachments/assets/71754dbc-2ae9-4d1c-8a31-acd656472fcf" />
**Retrospective Reserve** at Start of the 1st Year is always Zero

In other words, **Retrospective Reserve** at Start of the 2st Year = Expected Net Cash Flow at the end of the 1st year divided by the probability of surviving the 1st year

**Retrospective Reserve at Start of the Current Year** = Expected Net Cash Flow at the end of the Previous Year / Probability of Surviving in Previous Year+Reserves at the start of the Previous Year accumulated for one year divided by the Probability of Surviving in the Previous Year.
									

