# SBGP-0011: Dynamically Adjust Protocol Parameters
SolBlaze would like to propose a more dynamic strategy for adjustments to protocol parameters.

## Proposed Change
Under the current system, changing certain protocol parameters (such as various fees and requirements) involves a lengthy process of drafting a detailed proposal, waiting several days for a DAO vote to complete, and waiting even more days for changes to take effect across Solana epochs. However, we operate in a rapidly evolving space, where changes may need to be made in a more efficient manner. Our old processes for changes to protocol parameters have caused potential changes to stagnate and have impacted SolBlaze's ability to adapt to new trends in the liquid staking sector.

To strike a balance between the decentralized nature of DAO-based governance while avoiding the downsides of slow-moving processes, SolBlaze proposes that the DAO delegate discretionary authority to SolBlaze to adjust protocol parameters (in some cases within tight ranges), while ensuring the DAO maintains the right to revoke this authority at any time and has the power to veto discretionary changes through future proposals.

Specifically, here are the tight ranges associated with some protocol parameters:
- BlazeStake pool epoch commission: 0% - 5%
- Maximum validator staking rewards commission for the BlazeStake pool: 0% - 10%

Protocol parameters such as the threshold of stake where validator commission requirements change (currently set to 50,000 SOL in stake) which derive from the above parameters will still have to abide by those tight ranges.

Here are some examples where the dynamic adjustment of parameters makes the most sense:
- Continuing to run at 0% epoch commission is beneficial for upcoming DeFi strategies (such as SBGP-0010), but if TVL grows by significant amounts, setting a low commission of 1-2% can be beneficial to increase the size of the DAO treasury, and this commission can be dynamically increased or decreased based on fee revenues in other areas. On the other hand, during times of uncertainty such as black swan events, having a commission on the higher end of the range can provide more stability for continued sustainable operations.
- The maximum validator rewards commission for the pool is currently 0% for validators with over 50,000 SOL in stake who want to qualify for standard delegation stake and 10% in all other cases. At the time of that change, 50,000 SOL in stake at 0% commission was enough to run sustainably, but in the current market environment, that is no longer the case, so we may want to dynamically adjust that stake threshold value.
- Additionally, reducing the maximum commission for validators participating in our Custom Liquid Staking program can help ensure better pool APYs. We have already discussed with some validators receiving stake from the program and successfully encouraged them to lower their commissions, but having the ability to adjust that maximum commission will allow these changes to become more concrete.

As part of the responsibilities associated with this discretionary authority, SolBlaze will ensure that when parameters are changed, new values are included in the relevant docs within a 72-hour window to ensure transparency. Having discretionary authority over protocol parameters doesn't mean that SolBlaze won't still make future DAO proposals to adjust those parameters in situations where conditions are no longer evolving as rapidly or where changes would lead to significant impacts to users and/or partners, but rather that SolBlaze would have the capability to act more quickly and adjust to conditions that evolve on a day-to-day basis.

## Implementation Details
Since this proposal deals with delegation of authority at a governance and consensus level, no special implementations are immediately necessary.

## Voting
Yes - discretionary authority over protocol parameters will be delegated to SolBlaze in accordance with this proposal

No - protocol parameters that are currently under the authority of the DAO will continue to be under that authority

## Next Steps
If the proposal passes, the discretionary authority will be delegated in accordance with this proposal.

If the proposal fails, SolBlaze will discuss any shortcomings or concerns that caused this proposal to fail, make any necessary revisions, and submit a new proposal to the SolBlaze DAO.
