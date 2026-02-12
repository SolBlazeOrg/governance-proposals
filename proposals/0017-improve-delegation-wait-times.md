# SBGP-0017: Improve Delegation Wait Times
SolBlaze would like to propose an improvement to the Verified Validators Program to address the issue of long wait times for full approval delegation.

## Proposed Change
The current Verified Validators Program consists of a linear stake distribution system, where validators are accepted in batches over time for full stake, and validators that qualify as Candidates receive baseline stake while they wait in the queue. However, due to TVL bleeding, combined with potential institutional inflows drying up from the ongoing bear market, it has become increasingly difficult to accept batches on a more frequent basis, which has caused long delays for validators patiently waiting in the queue. 

To solve this issue, we propose changing the delegation strategy to a rotating system that allows for all eligible validators to receive full approval stake during some epochs. With this change, a certain number of batches will be selected as "active batches" to receive full stake for a period of 10 epochs. To start, we will likely have only one active batch for every 10 epochs, but as TVL increases, we can increase the number of simultaneous active batches accordingly. Once the 10 epoch period is over, we will incrementally rebalance stake to the next active batch such that the first validators in the next batch to receive new stake during the rebalance will be the first validators to be rebalanced out at the end of the 10 epoch period (to ensure that each validator gets 10 epochs of full approval stake while also allowing rebalancing to be spread across longer periods to preserve pool APY).

The validators outside of the active batch will continue receiving baseline stake until their rotation. Baseline stake will be an even distribution of remaining delegation, with 0% commission validators receiving twice as much baseline stake. At current TVL numbers, we estimate that baseline stake will increase from the current 500-1000 SOL amounts to approximately 1000-2000 SOL. This change will formally sunset the legacy algorithmic delegation strategy as all of that remaining stake will be redelegated as baseline stake. This adjustment will not impact the other segments of our delegation strategy such as Custom Liquid Staking and BLZE Gauges, which will continue to remain at their current percentage-based allocations.

Based on current validator revenue estimates and price data, validators will be able to accumulate approximately 3m BLZE during their 10 epochs of active batch stake and another 2m BLZE within 30-50 epochs of baseline stake (depending on commission) as a result of the increased revenue generated through stake from the Verified Validators Program, ensuring that the full veBLZE requirement to participate in the Verified Validators Program can be offset within 4 months (without even accounting for additional stake through the gauges). With these changes, validators can have more confidence in applying to the program and making the necessary contributions to participate in our protocol governance.

## Implementation Details

The improved delegation strategy will be added to the rebalancer bot after the passing of this proposal, and the active batch will be set to batch 2 (as batch 1 has already been fully staked for a while). As TVL fluctuates and time passes, the rebalancer bot will adjust baseline stake and active batches accordingly.

## Voting
Yes - the delegation strategy will be updated in accordance with this proposal

No - the delegation strategy will remain the same

## Next Steps
If the proposal passes, the delegation strategy will be updated in accordance with this proposal.

If the proposal fails, SolBlaze will discuss any shortcomings or concerns that caused this proposal to fail, make any necessary revisions, and submit a new proposal to the SolBlaze DAO.
