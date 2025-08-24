# SBGP-0015: Launch Liquid Governance Token
Votex would like to propose a launch of a liquid governance token called xBLZE, which represents BLZE max-locked in governance. This proposal was originally drafted by the Votex team and is being submitted on their behalf.

## Proposed Change
Votex and SolBlaze already have a strong partnership through the veBLZE votes market, where SolBlaze users can delegate their locked veBLZE and validators can buy voting power that can be used in the BLZE Gauges ([votex.so/daos/solblaze](https://votex.so/daos/solblaze)). Right now, 200m veBLZE is delegated to the votes market, generating annualized APR ranging from 16% to 74%. Building on this collaboration, Votex proposes to launch xBLZE, a liquid representation of BLZE max-locked in governance. Users will be able to:
- **Stake liquid BLZE and mint xBLZE**, which represents a liquid version of veBLZE (BLZE max-locked in governance)
- **Deposit xBLZE to a dedicated rewards pool**. This pool will receive vote power buys from the veBLZE votes market, where validators purchase veBLZE voting power in order to participate in the BLZE Gauges

This creates a liquid, market-driven system around BLZE governance power, while preserving the max-lock effect of veBLZE, unlocking more potential for SolBlaze users.

As an overview, Votex is building the first-ever vote market infrastructure on Solana, with live integrations for SolBlaze and Saber delegated votes markets. The next phase introduces **Liquid Governance Tokens (LGTs)**, liquid representations of positions max-locked in governance, enabling both greater accesibility and new forms of market/governance utility.

For SolBlaze, this means:
- xBLZE is the liquid version of veBLZE
- There is more potential in the veBLZE votes market, where validators can acquire governance power in the BLZE Gauges by buying veBLZE votes
- Rewards from this vote market flow to xBLZE stakers, creating direct incentives for participation and unlocking utilities for BLZE
- As a tokenized representation, xBLZE can unlock new use-cases in DeFi

How xBLZE would work:
- xBLZE represents a max-locked BLZE position (veBLZE)
- BLZE holders can mint xBLZE and freely trade or hold it as a liquid governance token
- A liquidity pool will be created for xBLZE, allowing swaps between xBLZE and BLZE
- Users who deposit xBLZE into the dedicated xBLZE rewards pool earn rewards derived from validators purchasing veBLZE voting power in the votes market
- This creates a recurring economic flywheel: validators buy votes to get more stake, giving them revenues that they can use to continue buying votes, while xBLZE stakers receive a portion of these validator revenues as rewards

Why this matters for the SolBlaze ecosystem:
- **Accessibility:** users can participate in veBLZE governance without committing to illiquid locks
- **Liquidity:** xBLZE enables the trading of governance power, making BLZE governance more flexible
- **Validator Incentives:** validators gain an additional veBLZE market to compete for governance weight in the BLZE Gauges
- **Solana Ecosystem Expansion:** SolBlaze will establish itself as one of the first DAOs to adopt liquid governance tokens tied to active vote markets

To ensure efficient development and smooth integration, Votex requests that 200m BLZE from the DAO fee revenues be used as initial liquidity to bootstrap xBLZE. Liquidity will be deployed as single-sided BLZE into a 1-bin DLMM on Meteora, ensuring BLZE liquidity for xBLZE. All LP fees generated from this liquidity will be compounded back into the pool in the form of xBLZE and/or BLZE, which both increases the xBLZE liquidity and grows the market for veBLZE voting power.

## Implementation Details

We will coordinate the launch of the xBLZE liquid governance token with Votex and assist with the deployment of 200m BLZE into the Meteora liquidiy pool. Once the liquidty has been bootstrapped, the Votex team will be able to enable xBLZE and the corresponding components of the liquid governance token in conjunction with their existing veBLZE votes market.

## Voting
Yes - 200m BLZE from DAO fee revenues will be used to bootstrap xBLZE liquidity

No - DAO fee revenues will not be used to bootstrap xBLZE liquidity

## Next Steps
If the proposal passes, the 200m BLZE will be deployed as liquidity according to this proposal.

If the proposal fails, Votex will discuss any shortcomings or concerns that caused this proposal to fail, make any necessary revisions, and submit a new proposal to the SolBlaze DAO.
