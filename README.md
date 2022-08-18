# Realized-GARCH
Incorporating a realized measure of volatility into a standard GARCH(1,1) model

In an extension to our initial HAR-RV model, we include a Realized GARCH model (GARCH-x), which is simply a GARCH(1,1) with a Realized Volatility measure as an additional exogeneous variable; in this case we'd be using a 5-min RV. This is performed in the spirit of Hansen, Huang, Shek (2010) Realized GARCH: A Complete Model of Returns and Realized Measures of Volatility. Theoretically GARCH-x updates faster than the standard GARCH:

![image](https://user-images.githubusercontent.com/105033135/185288641-0c40cb56-e31f-4948-90bb-ecc0e6bf3df9.png)

Using the same dataset as before (i.e. the FBMKLCI Bursa Malaysia index futures), our empirical analysis shows a weaker performance for GARCH-x vs. HAR and the conventional GARCH. We do not rule out modelling errors as the arch_model library used may be ill adapted for the Realized GARCH model (unlike R's rugarch package). 

![image](https://user-images.githubusercontent.com/105033135/185289116-970603a3-6b00-48a5-a002-86cb2fb85bf5.png)

![image](https://user-images.githubusercontent.com/105033135/185289145-20aa83a8-0256-4be8-baf8-b08f6a3a6e6d.png)
