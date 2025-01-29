# SBGP-0009: Increase Pool APY
SolBlaze would like to propose a variety of changes to the delegation strategy and BlazeStake pool parameters to increase the APY of the pool while still supporting a wide range of validators.

## Proposed Change
In an increasingly competitive liquid staking environment, bSOL currently has a lower APY compared to other alternatives, including LSTs launched on Bliq. This lower APY is in part due to SolBlaze's relaxed rules on its standard delegation strategy, which stakes to higher commission validators (unlike other pools such as Jito and effectively Marinade which force 0% or in some cases negative commission) in order to support the validator ecosystem. These changes to the delegation strategy seek to maintain that spirit while also focusing on growing bSOL stake through increased APYs, which only further supports validators.

Within the standard delegation strategy, BlazeStake should only stake to 0% commission and 0% MEV commission validators (note: not running a MEV client is equivalent to having 100% MEV commission), unless the validator has under 50,000 SOL in stake. This change only impacts the standard delegation strategy (also known as baseline stake) and will not affect Custom Liquid Staking or BLZE Gauges. Under current network conditions, 50,000 SOL in stake is enough to exceed the break-even point for validator economics, so this change will allow us to continue supporting newer and smaller validators while preventing already profitable validators from taking up more pool stake. Additionally, by removing the high commission validators, more stake will be distributed to the lower commission validators instead.

Furthermore, the SolBlaze pool should drop its epoch commission to 0% in order to maximize the potential APY and stay competitive with other 0% and negative commission LSTs. As part of this proposal, we will temporarily drop the commission to 0% until March 1st, unless another proposal passes to extend this 0% commission period. Over the next month, we hope to grow Bliq through a series of key partnerships to bring in consistent revenue to the DAO that can offset the lost revenue from commission on BlazeStake.

Lastly, we should add a dedicated section of the delegation strategy that is reserved only for high-performance validators. 20% of the standard delegation will go towards only 0% commission and 0% MEV commission validators which are picked at SolBlaze's discretion based on factors relating to their APY and contributions to the network.

Breakdown of current delegation strategy and pool parameters:
- 70% algorithmic strategy (distributed across hundreds of validators with the goal of increasing decentralization of the network)
- 20% BLZE gauges (allows BLZE holders to vote on which validators should receive this stake through the BLZE gauge-based voting model)
- 10% BlazeBoost matching pool (used to boost stake done through Custom Liquid Staking as an incentive for validators to promote BlazeStake usage)
- 5% epoch commission (2.5% to SolBlaze and 2.5% to the SolBlaze DAO)

Breakdown of new delegation strategy and pool parameters:
- 50% algorithmic strategy (distributed across hundreds of 0% commission and 0% MEV commission validators or small validators with the goal of increasing decentralization of the network)
- 20% BLZE gauges (allows BLZE holders to vote on which validators should receive this stake through the BLZE gauge-based voting model)
- 20% high performance (distributed across high APY validators who are contributing positively to the network and maintaining 0% commission + 0% MEV commission)
- 10% BlazeBoost matching pool (used to boost stake done through Custom Liquid Staking as an incentive for validators to promote BlazeStake usage)
- 0% epoch commission until March 1st (unless a future proposal is made to extend the 0% commission period)

## Implementation Details
The new delegation strategy will be added to the rebalancer bot after the passing of this proposal, and the pool will incrementally shift stake away from high-commission validators and towards higher-performing validators over the next few epochs. Additionally, the epoch commission will be lowered to 0% and increased back to 5% on March 1st, unless a future proposal is made to extend the 0% commission period.

## Voting
Yes - the delegation strategy and BlazeStake pool parameters will be updated in accordance with this proposal

No - the delegation strategy and BlazeStake pool parameters will remain the same

## Next Steps
If the proposal passes, the delegation strategy and BlazeStake pool parameters will be updated in accordance with this proposal.

If the proposal fails, SolBlaze will discuss any shortcomings or concerns that caused this proposal to fail, make any necessary revisions, and submit a new proposal to the SolBlaze DAO.
