# ***The Nelson and Siegel Model Of the Term Structure***

**Key Topics Covered**

* **Estimating the term structure with Nelson-Siegel model**  
    
  * Defining the model.  
  * Accessing data for specific dates from FEDInvest page of TreasuryDirect site.  
  * Estimating the model.  
  * Using the model to estimate forward rates and par yields for arbitrary dates.  
    

    
* **Python concepts:**  
    
  * SciPy optimize module estimtes Nelson and Siegel model  
  * NumPy arrays  
  * Pandas  
  * Accessing bond price data from FEDInvest page of TreasuryDirect    
  * Custom modules.  
    * accruded\_interest  
    * create_payoff_matrix  
    * scheduled\_pay\_dates  
    * adjust\_bond_pay_dates  
    * one\_y\_axis  
  * FEDInvest developed in the chapter and added to the custom module

## ***Background***

This chapter's examples and discussions rely on the **Pandas** and **NumPy** libraries.

* **Pandas** is introduced in [*A Quick Introduction to Pandas*](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/An_Introduction_To_Pandas.html#a-quick-introduction-to-pandas).  
* **NumPy** is introduced in [*A Quick Introduction to NumPy*](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/An_Introduction_To_NumPy.html#a-quick-introduction-to-numpy).  
* The accruded\_interest function is imported from [Chapter Two](https://patrickjhess.github.io/Imported-Functions/accrued_interest.html#accrued-interest-is-a-helper-function-that-calculates-accrued-interest)  
* The create_payoff_matrix function is imported from [Chapter Four](https://patrickjhess.github.io/Imported-Functions/create_payoff_matrix.html#create-payoff-matrix-helper-function)  
* The scheduled\_pay\_dates function is imported from [Chapter Three](https://patrickjhess.github.io/Imported-Functions/scheduled_pay_dates.html#scheduled-pay-dates)   
* The adjust\_bond_pay_dates function is imported from [Chapter Three](https://patrickjhess.github.io/Imported-Functions/adjust_bond_pay_dates.html#adjust-bond-pay-dates)  
* The one\_y\_axis function is imported from [Chapter One](https://patrickjhess.github.io/Imported-Functions/one_y_axis.html)  
* Additional relevant Python concepts can be found in the introductory volume, [*Background Material: An Introduction to Python for Financial Python*](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/intro.html), that relate to this and other chapters of *Basic Concepts of Fixed Income*.

**The chapter includes Five  sections:**

1. *Why Nelson and Siegel*  
     
   * develops the model  
   * describes the parameters
   * relation of parameters to spot rates of interest

   

2. The Jupyter notebook *Accessing Treasury Bill Prices From Treasury Direct Website*  
   * devlops the function FEDInvest that sends a post reqyest to FEDInvest page and returns data for a specified data  
   * cleans up the data returned data of FEDInvest

   

3. The Jupyter notebook *Estimating The Nelson and Siegel Model*  
    * estimates the Nelson and Siegel model with data from the FEDInvest page of TreasuryDirect  
    * usees model estimates to calculate forward rates for arbitrary dates   
    * uses model estimates to calculate par yields for arbitrary dates  
    
 
5. *Summarizing the results of The Nelson and Siegel Model Of the Term Structure*  
6. *Functions Imported by Chapter Nine* describes the function imported from DropBox (*module\_basic\_concepts\_fixed\_income*).

