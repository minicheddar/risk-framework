# Protocol Risk Asessments

## 1. Risk Identification
During the risk identification stage all risks are collected and listed according to the affected role (e.g. node operator, swapper, liquidity provider). As a starting point the [Risk Registry](../risk-registry.md) can be used. The results are used in the risk analysis stage.

## 2. Risk Analysis
Our methodology relies on the qualitative risk analysis. The project's explicit and implicit risk mitigation strategy has to be analyzed. Therefore, for each identified risk it is necessary to understand if the risk is accepted, monitored, mitigated, transferred or eliminated.

Given the risk mitigation strategy the probability (left column) and severity (first row) the resulting residual risk (cell value) has to be estimated based on the following definition:

| Probability/Severity                    | Neglible (less than 1% of TVL affected) | Marginal (1-5% of TVL affected) | Critical (6-25% of TVL affected) | Catastrophic (more than 25% of TVL affected) |
|-------------------------------------------|-----------------------------------------|---------------------------------|----------------------------------|----------------------------------------------|
| Certain (expectation > 75% probability)   | High                                    | High                            | Very High                        | Very High                                    |
| Likely (75% >= expectation > 50%)         | Medium                                  | High                            | Very High                        | Very High                                    |
| Possible (50% >= expectation > 25%)       | Low                                     | Medium                          | High                             | Very High                                    |
| Unlikely (25% >= expectation > 5%)        | Low                                     | Low                             | Medium                           | High                                         |
| Rare (5% >= expectation)                  | Low                                     | Low                             | Low                              | Medium                                       |
| Eliminated                                | None                            | None                       | None                                 | None                                             |


With respect to protocol cove smart contract and governance risks are the main sources for potential claims. The [Security Maturity Level project](https://github.com/NexusRiskHub/security-maturity-level) regularly validates measures such as audits, bug bounties, TVL exposure, and governance time-lock, which are the main parts of a successful mitigation strategy. The maturity level can be directly mapped to the probability as follows:

| Security Maturity Level | Mapped Probability |
|-------------------------|--------------------|
| 0                       | Certain            |
| 1                       | Likely             |
| 2                       | Possible           |
| 3                       | Unlikely           |
| 4                       | Rare               |
| 5                       | Rare               |


If the protocol uses other mitigation measures such as a "reimbursement treasury", then the probability of a claim is reduced and the risk should be reduced accordingly (depending on the treasury's size).

Additional sources can be also involved in the risk analysis process to estimate probabilities or impacts, such as:
* https://github.com/ConsenSys/defi-score
* https://docs.aave.com/risk/asset-risk/methodology
* https://inspect.codefi.network/
* https://github.com/defi-defense-dao/defi-risk-tools-list


## 3. Risk Evaluation
The purpose of risk evaluation is to support decisions. Risk evaluation involves comparing the results of the risk analysis with the established risk criteria to determine the risk assessor's **staking parameters**, where the highest identified risk should be decisive for the staking parameters. Based on the risk assessor's risk appetite, different allocations can be done:

As an example, a **conservative risk assessor** may allocate the stake as follows:
 1. 100% staking for low risk protocols
 2. 75%  staking for low-medium risk protocols
 3. 25%  staking for medium risk protocols

As a further example, a **risk tolerant risk assessor** may stake as follows:
 1. 100% staking for low risk protocols
 2. 100% staking for low-medium risk protocols
 3. 50%  staking for medium risk protocols
 4. 25%  staking for high risk protocols
