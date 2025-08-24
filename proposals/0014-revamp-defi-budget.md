# SBGP-0014: Revamp DeFi Budget
SolBlaze would like to propose a complete revamp of our DeFi budget to streamline the experience for both users and DeFi protocols.

## Proposed Change
Our current DeFi budget is funded by the initial vesting allocation of BLZE tokens from TGE, which unlock every week and halve every 24 weeks according to the distribution schedule. However, after several halving cycles, the weekly unlock for the DeFi budget is now no longer enough to sustain competitive emissions in the DeFi ecosystem.

As a result, we propose allocating 500m BLZE from the DAO's fee revenues to establish a proper budget for DeFi incentives over the next three months, with a soft cap of 40m BLZE per week in emissions averaged across the three month period. Our current emissions targets don't exceed this cap currently, and we have been reallocating emissions where appropriate with guidance from our risk management and allocation strategy partners to ensure the most optimal emission amounts to build sticky TVL while avoiding overpaying for incentives. With these measures, it's possible that we could extend the budget to last substantially longer than the initial timeframe, and/or we could use the excess emissions up to the soft cap to expand the scope of our emissions in the DeFi ecosystem.

With this change in the DeFi budget system, we are also formalizing our decision to fully sunset the non-validator gauges (such as the DeFi pools on the gauges). User behavior has shown that the main use-case for the BLZE Gauges has been for directing stake to validators, and having a DeFi component of the gauges model adds extra complication both for BLZE users and for the DeFi protocols who have to adjust emissions across pools on a weekly basis in accordance with gauge allocation fluctuations. Our newly revamped website will only have validator gauges, and we will internally deprecate and remove any votes to gauges not aligned with validator stake. Note that this change will not cause any immediate changes in the vote distribution to existing validators in the gauges, as the votes to non-validator gauges will simply be redelegated to the "Discard Votes" virtual gauge until a user either moves their votes to a validator or delegates their voting power to a vote marketplace such as Votex.

Furthermore, there are some upcoming changes to Pyth's oracle funding model that the DAO needs to address. When Pyth switched to their new oracle model around a year ago, they covered initial costs for the bSOL and BLZE Sponsored Feeds for the first year given how the Solana DeFi ecosystem relies on these oracle feeds to secure substantial TVL in various protocols. However, they are now requesting that providers cover costs for Sponsored Feeds to ensure long-term sustainability in their operations. The costs for maintaining the bSOL and BLZE Sponsored Feeds total to approximately 100 SOL per year, paid in installments. We propose using 50 bSOL from DAO fee revenues, which should be enough to cover the first installment with plenty of buffer, leaving the remainder to use towards subsequent installments. Additionally, we propose that the DAO authorizes SolBlaze to pre-allocate enough funds from ongoing DAO fee revenues to cover future installments over the years (to avoid duplicate proposals).

## Implementation Details

We will coordinate the new emissions system with our partners in the DeFi ecosystem, perform the steps necessary to deprecate the non-validator gauges, and ensure that we continue to meet the funding obligations associate with our Pyth Sponsored Feeds.

## Voting
Yes - the DeFi budget will be revamped in accordance with this proposal

No - the DeFi budget will remain the same

## Next Steps
If the proposal passes, the DeFi budget will be revamped in accordance with this proposal.

If the proposal fails, SolBlaze will discuss any shortcomings or concerns that caused this proposal to fail, make any necessary revisions, and submit a new proposal to the SolBlaze DAO.
