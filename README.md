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
