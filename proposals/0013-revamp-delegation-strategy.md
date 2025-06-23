# SBGP-0013: Revamp Delegation Strategy
SolBlaze would like to propose a complete revamp of the BlazeStake delegation strategy with a focus on eliminating sybils and delegating more stake to high-quality validators with a track record of ecosystem contributions.

## Proposed Change
Our current delegation strategy is the most open and inclusive of any stake pool on Solana, allowing for any validator that meets bare-minimum requirements to quickly gain baseline stake. However, the low barrier to entry has made BlazeStake a target for likely sybils, where validators with similar stake profiles and similar funding strategies request to join the pool at similar times. Since we have no concrete proof of these validators being sybils (and given that most of them have passed SFDP KYC), we cannot take any direct action, but it's clear that our delegation strategy must be refocused. Although we want to maintain our position of being the staker of last resort for new validators trying to get started, we should also reward the dedicated efforts of unique validators contributing positively to the Solana ecosystem.

Therefore, SolBlaze proposes the introduction of a SolBlaze Verified Validators program, where validators can apply by providing examples of their contributions to the ecosystem (a much stronger anti-sybil measure compared to KYC, where people can run sybils by having friends and family members KYC on their behalf or by purchasing KYC identities). To increase alignment with the SolBlaze ecosystem and add a financial disincentive to applying with sybils, validators who want to join the SolBlaze Verified Validators program will need to hold a certain amount of veBLZE (initially 5m veBLZE but may be dynamically adjusted in accordance with SBGP-0011) in a unique wallet. This veBLZE requirement is fairly minimal compared to the additional revenue from getting increased stake, and it will help reduce spam and low-quality applications.

Once validators have been accepted into the SolBlaze Verified Validators program, they will be eligible for larger quantities of stake from BlazeStake (targeting >10k SOL tranches of stake). In order to improve stake distribution within the pool, validators who do not already have outsized stake from BlazeStake through Custom Liquid Staking and BLZE Gauges will be prioritized for these elevated stake allocations, and if the queue is oversubscribed, additional factors like geographic decentralization, commission, and existing stake levels may be taken into account when determining queue priority.

We will make the list of SolBlaze Verified Validators accessible through an API so that other staking entities can use the list to curate their own delegation strategies to include high-quality validators. If SolBlaze Verified Validators are caught attempting to submit applications for their sybils or otherwise conducting malicious behavior, they will be banned and blacklisted from the program, and this blacklist will also be publicly accessible through an API.

Under the authority granted to SolBlaze from SBGP-0011, we will dynamically increase the allocation of stake to SolBlaze Verified Validators and decrease the allocation to baseline stake, while still leaving some allocation to baseline stake to help new validators. Note that this proposal mainly impacts the algorithmic strategy and will not have any effect on the percentages for stake through BLZE Gauges or the BlazeBoost matching pool for Custom Liquid Staking.

## Implementation Details

The new delegation strategy will be added to the rebalancer bot after the passing of this proposal, and the application form to become a SolBlaze Verified Validator will be released to the public. As validators are accepted into the program, the rebalancer bot will shift stake accordingly.

## Voting
Yes - the delegation strategy will be updated in accordance with this proposal

No - the delegation strategy will remain the same

## Next Steps
If the proposal passes, the delegation strategy will be updated in accordance with this proposal.

If the proposal fails, SolBlaze will discuss any shortcomings or concerns that caused this proposal to fail, make any necessary revisions, and submit a new proposal to the SolBlaze DAO.
