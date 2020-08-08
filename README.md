# Gnosis-fork-hack
A repo pulling together our theory, design, and progress made on our Gnosis Conditional Token hack for Fork the World. We attempted to add futarchy in our operational decision making for our DAO.

Aim:
To integrate the Gnosis Conditional Token Framework (CTF) into an Aragon DAO structured around our EthDenver project CastleDAO (https://devfolio.co/submissions/castle-dao and https://github.com/johnkozan/housing-dao). 

Integrating the CTF served as a multipurpose solution for several issues that still existed in our original project design.

        1. There was little use for the token besides buying and selling on the bonding curve.
        - Integrating a Conditional Token with the collateral being the housing token both adds functionality to the token and ensures that participants in the governance are active holders of the housing token already.

        2. There was little incentive for token holders to be active in the governance process at all.
        - By adding the conditional tokens as a governance mechanism, token holders are incentivised to participate in the governance process.

        3. There were no measures to ensure that token holders who did engage in governance processes were incentivized toward good governance outside of the overall value of the token.
        -  Adding conditional tokens also allows governance participatns to be rewarded for engaging in good governance, while pruning the holdings of those who consistently perform poorly in the governance market.

System Design:
We hoped to deploy an Aragon DAO on Rinkeby and install the CTF as an app. We sketched several options for how this could be structured, and decided that since the council is already a trusted body for the DAO and can be set with multisig requirements, it would act as a centralized oracle for the market conditions. Because governance outcomes of a specific DAO on real world assets is difficult to verify in an oracle context, it is unlikely that an oracle (particularly a decentralized one) would be available. Because the market is isolated to token holders in the DAO, we think that this is an acceptable level of trust to give the DAO council multisig.

we intend to use the conditional token more for decisions like whether to renovate a suite or not, increase or lower rent, authorize advertising, etc - operational decisions - less based on a predictive market per-se, but an incentivized approach to making good governance decisions for the DAO.
In this way we intend to 
- gain a mechanism by which DAO members are ensured more responsible operational management through incentives without required effort by all members in governance.
- Offer a use for the bonded token on top of the bonding curve and ownership aspects, as it will be used as collateral for the conditional tokens.
- Offer DAO members potential to earn more tokens without having to buy or sell into the bonding curve
- Incentivize self-selected, engaged, and effective individuals for governance decisions
- Disincentivize and weed out ineffective individuals from governance decisions through loss of value in their conditional tokens.

Example Conditional Questions:
Rent increase/decrease question: 
"If we lower the rent of unfilled suite by $100/month, will the suite be filled with new tenants next month" 
or 
"If we raise the rent by $100, we will retain our current tenants"
An operational decision with a conditional outcome that is tied to the token market when initialized.

Renovate or Not question:
"If we renovate, we will earn back the expenditure in 12 months"
"If we renovate, the value of the property will be 2% higher in 2022."

"This specific area has average house values of $xxx,000. If we purchase an asset there, it will hold at least 98% of that value for 2 years"
(longer term question with potential for less centralized oracle data)


Progress:
Because this hack focused on the futarchy aspect of the DAO, we opted for deploying a fundraising DAO with a fairly standard Bancor curve, and looked into installing an app. The actual installation of the CTF as an Aragon app took us longer than anticipated, and so we did not progress to a fully functioning futarchy governed DAO, but the design and many of the tools are in place.


Blockers:
We ran into a versioning issue 

We really considered forking Luzzif's awesome implementation of conditional markets as an Aragon app (https://github.com/luzzif/aragon-prediction-markets) and changing the collateral for our purposes, but decided against it since he's in this same category in the hackathon. Great work on it! 

