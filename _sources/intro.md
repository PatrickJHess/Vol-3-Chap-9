# Financial Python

## Volume: Basic Concepts of Fixed Income

### Chapter Nine: The Nelson and Siegel Model Of the Term Structure

Bootstrapping allows us to determine spot and forward interest rates for specific, discrete dates. Although this provides valuable insight into the current market and future expectations, the resulting data lacks the granularity needed for pricing financial instruments that mature on intermediate dates. Interpolation is necessary to bridge the gaps.

Furthermore, the quality of the data used for bootstrapping presents a challenge. Non-coincident bond prices lead to relative price discrepancies compared to the theoretical present value. Least-squares estimation can mitigate some pricing errors, it may not eliminate obvious flaws like negative forward rates. A professional trading desk would exclude stale or questionable prices, but our approach is agnostic to data quality. To address this, we benefit from imposing a structural constraint on the interpolation that prevents implausible outcomes. The Nelson and Siegel model achieves this by offering a parsimonious solution based on three fundamental characteristics of the term structure:

* The level  
* The slope  
* The shape

This chapter introduces and estimates the Nelson and Siegel model. The resulting estimates are then used to calculate forward rates and par yields for arbitrary dates.
