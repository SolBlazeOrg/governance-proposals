# SBGP-0001: Stake Gauges
SolBlaze would like to propose a change to the BlazeStake standard delegation strategy where 10% of stake under this strategy would be controlled by a novel gauge-based voting system.

## Proposed Change
The current breakdown of the BlazeStake standard delegation strategy is as follows:
- 90% algorithmic strategy (distributed across hundreds of validators with the goal of increasing decentralization of the network)
- 10% BlazeBoost matching pool (used to boost stake done through Custom Liquid Staking as an incentive for validators to promote BlazeStake usage)

The new BlazeStake standard delegation would follow this breakdown:
- 80% algorithmic strategy (distributed across hundreds of validators with the goal of increasing decentralization of the network)
- 10% BlazeBoost matching pool (used to boost stake done through Custom Liquid Staking as an incentive for validators to promote BlazeStake usage)
- 10% BLZE gauges (allows BLZE holders to vote on which validators should receive this stake through a novel gauge-based model)

### Gauge Voting Structure
The vote weights for gauges would be equivalent to the voting power for locked BLZE (veBLZE) in Realms. Depositing 1 BLZE into Realms gives a user a voting power of 0.1 veBLZE, while locking 1 BLZE in Realms for the maximum length (currently set to 5 years) gives a user a voting power of 1 veBLZE (a 10x multiplier compared to unlocked BLZE deposited into Realms). For any locking period between fully unlocked and the maximum length, the amount of veBLZE in voting power scales proportionally, so locking for a longer period of time is linked to having a higher veBLZE voting power.

Gauges votes would be applied in one-week increments. The votes would be tallied at the end of each week-long voting period, and the pool rebalancer would shift the stake in the BlazeStake pool accordingly as part of standard rebalancing procedures. Votes would not expire and could be updated at any point during the week, but they would only be finalized for the purposes of stake distribution at the end of each week-long voting period.

## Implementation Details
Since Realms does not currently have a built-in gauges system, SolBlaze has decided to create a custom gauge voting platform. SolBlaze has developed a first-of-its-kind snapshot system to atomically record voting weights in Realms registered through the Voter Stake Registry (VSR) plugin at a certain block height. BLZE holders who have deposited their BLZE into governance on Realms (and locked their BLZE for a certain amount of time if applicable) are automatically picked up by the custom snapshots system, which calculates the appropriate veBLZE voting weights. Users would be able to then submit their gauge votes through a gauges interface on the SolBlaze website, and their veBLZE voting power would be proportionally split across these gauges according to the user's preference.

## Voting
Yes - The delegation strategy will be updated in accordance with this proposal

No - The delegation strategy will remain unchanged

## Next Steps
If the proposal passes, the gauges will be released during the same week, pending any final preparations or last-minute bugfixes for issues caught during testing. Stake in the pool will be rebalanced according to the new standard delegation strategy once the first weekly veBLZE vote weight snapshot is taken for the gauges.

If the proposal fails, SolBlaze will discuss any shortcomings or concerns that caused this proposal to fail, make any necessary revisions, and submit a new proposal to the SolBlaze DAO.
