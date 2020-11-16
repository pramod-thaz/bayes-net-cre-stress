# Methodology Primer
The analytical foundation of this exercise is based on Real Estate Econometric Forecast's (REEFM)<sup>1</sup> econometric model for the integration of real estate's space and capital markets. The intention is not to use the econometric models or equations but to use it as a conceptual framework to identify the causal relationships between macro-economic factors and space market variables.



# Traditional Approaches to Stress Testing
Various approaches (e.g. the extreme-tail approach or vulnerability approach) have been formulated and applied for traditional asset classes. These rely on econometric models built on past data or are based on simulations where the parameters are derived from past observations. 

Stress testing approaches to CRE portfolios have been rather cursory, one-dimensional or complex. Usually they are one of the following:

1. High level subjective adjustments or “haircuts” to value and NOI
2. Derive CRE market assumptions using econometric models ( engaging CRE data firms such as CoStar) to develop space market and capital market “stressed” projections (MLA) for key markets by using stressed macro-financial time series as inputs.



# Limitations
Risk management, portfolio allocation and, in general, the strategic analysis of financial and economic outcomes share the common unstated assumption that the past conveys useful statistical information about the future. In normal market conditions, such assumptions that underpin these statistical analyses work well, and are perhaps justifiable over a short time horizons (with identical regimes) where we can assume parameter stability. But such relationships seldom hold true under stressed scenarios.

This is particularly true in the case of current economic crisis due to a pandemic. We haven't had a pandemic in over a hundred years which limits availability of relevant data. Additionally, the primary cause of disruption and uncertainty this time around is in the service economy rather than the financial economy like we have seen in more recent downturns.

Specifically, the approaches mentioned above for CRE have the following limitations:

1. High level haircuts while easy are unable to provide coherent traceback to macro-financial stress variables
2. Stress tests that depend on data sourcing and curating via 3rd party data providers are expensive, time-consuming, and need asset valuation models. 
3. Econometric models require a long time to build and require numerous adjustments for non-covariance stationarity and other statistical anomalies. 

# Additional Considerations

It would be desireable to have a methodology:

1. That didn't depend on costly procurement of data 
2. Can be performed with open source software
3. That is intuitive and parsimoniuos
4. Can incorporate expert judgement


# Proposed Methodology
We propose and implement a coherent stress testing approach that recognizes the limitations stated above and accomplishes the following:

1. One or more root-causes indicated as macro-financial variables (e.g. Real GDP growth & Unemployment Rate)
2. Identification of transmission channels and causal relationships. The latter is too important to be ignored.
3. Ability to incorporate subjective or expert assessment (probabilistic) in how these transamission channels are linked together.

## Bayesian Networks
Bayesian networks (BN) are graphical models that represent a set of random variables for a given problem, and the probabilistic relationships between them. They offer a mathematical model for representing knowledge & uncertain information and enables causal reasoning – i.e. in this case from macroeconomic variables to asset value.

For this exercise we need a mix of predictive and combined reasoning - reason from new information about causes (e.g. Unemployment) to Effect (e.g. NOI, Value change of an asset) following the direction of causality and inference.


## Advantages

1. Constructed using expert opinion & subjective assessment 
2. Can incorporate asset level idiosyncrasies due to tenancy profile, capex needs etc.
3. Intuitive, logically coherent description of complex stress scenario.
4. Ability to extend and add complexity/variables as desired. 
5. Transparent and Understandable – no black box, or dependency on 3rd party models.
6. Can be used to reverse stress-test. E.g. which set of macro-economic conditions can lead to a X percentage decline in capital values.
7. Base form deliverable can be coded in Python/R; no immediate need for new software

## Disadvantages
The temporal dimension has not been modeled. These scenaris are path dependant and this exercise omits that for sake of brevity.


## Post Procecessing

The model variables will be instantiated with categorical variables to decouple model construction and calbration. The categorical variables (e.g. low, medium, high for capital value change distributions) will then be calibrated to opinions of internal experts as well as data published in external reports. 

## Disclaimer
This project is only an experiment and a Proof-of-Concept of using Bayesian Networks to stress test a CRE portfolio. We do not accept any responsibility for any losses incurred with the use of the model.
