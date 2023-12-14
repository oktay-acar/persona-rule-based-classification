# Calculating Lead-Based Returns with Rule-Based Classification using Persona's Dataset

**Business Problem**

A game company wants to create level-based new customer definitions *(persona)* by using some features of its customers, and to create segments according to these new customer definitions and to estimate how much the new customers can earn on average according to these segments.

For Example: It is desired to determine how much a 25-year-old male user from Türkiye who is an IOS user can earn on average.

**Dataset Story**

The **persona.csv** dataset contains the prices of the products sold by an international game company and some demographic information of the users who buy these products. The dataset consists of records created in each sales transaction. This means that the table is not deduplicated. In other words, a user with certain demographic characteristics may have made more than one purchase.

**Variables**
- **PRICE:** Customer spending amount
- **SOURCE:** The type of device the customer is connecting with
- **SEX:** Gender of the customer
- **COUNTRY:** Country of the customer
- **AGE:** Age of the customer

**Before Application:**
| &nbsp; | PRICE | SOURCE  |  SEX  | COUNTRY |  AGE  |
| :----: | :---: | :-----: | :---: | :-----: | :---: |
|   0    |  39   | android | male  |   bra   |  17   |
|   1    |  39   | android | male  |   bra   |  17   |
|   2    |  49   | android | male  |   bra   |  17   |
|   3    |  29   | android | male  |   tur   |  17   |
|   4    |  49   | android | male  |   tur   |  17   |

**Expected Output:**
| &nbsp; |  customers_level_based   |  PRICE  | SEGMENT |
| :----: | :----------------------: | :-----: | :-----: |
|   0    | BRA_ANDROID_FEMALE_0_18  | 35.6453 |    B    |
|   1    | BRA_ANDROID_FEMALE_19_23 | 34.0773 |    C    |
|   2    | BRA_ANDROID_FEMALE_24_30 | 33.8639 |    C    |
|   3    | BRA_ANDROID_FEMALE_31_40 | 34.8983 |    B    |
|   4    | BRA_ANDROID_FEMALE_41_66 | 36.7371 |    A    |

---

## Requirements
~~~python
pandas==1.5.1
~~~

---

## Author
[Oktay Acar](https://github.com/oktay-acar)