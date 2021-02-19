# Liquity smart contracts bug bounty

A bug bounty for the smart contracts of the Liquity protocol is now live. We intend for hackers to look for smart contract vulnerabilities in our system that can lead to loss of funds or locked components.

## Rewards

Vulnerability reports will be scored using the  [CVSS v3](https://www.first.org/cvss/) standard. The reward amounts for different types of vulnerabilities are:

### :bug: "**Critical** (CVSS 9.0 - 10.0)"
    $5,000 - $50,000

### :rotating_light: "**Major** (CVSS 7.0 - 8.9)"
    $2,500 - $5,000

### :zap: "**Medium** (CVSS 4.0 - 6.9)"
    $1,000 - $2,500

### :warning: "**Low** (CVSS 1.0 - 3.9)"
    $500 - $1,000

Rewards will be awarded at the sole discretion of Liquity AG. Quality of the report and reproduction instructions can impact the reward. Rewards are denominated and paid out in USD.

For this initial bug bounty program, there is a **maximum bounty pool of $250,000**.

The bug bounty program is ongoing and has been running since February 19th, 2021.

## Reporting

### :writing_hand: Reporting a found vulnerability
Please responsibly disclose any findings to the development team, following these instructions:

- In order to report a vulnerability, please write an email to `security@liquity.org` with [SECURITY DISCLOSURE] in the subject of the email.
- For sensitive vulnerabilities, please the encrypt the email using this [PGP key](https://keys.openpgp.org/vks/v1/by-fingerprint/3F21FFCDAD2A7D5B8E113198FCE791AE1A6F4793) (Fingerprint: `FCE7 91AE 1A6F 4793`)
- We will make our best effort to reply in a timely manner and provide a timeline for resolution.
- Please include a detailed report on the vulnerability with clear reproduction steps. The quality of the report can impact the reward amount.


Failure to do so will result in a finding being ineligible for any bounties.

## Scope

In scope for the bug bounty are all the smart contract components of the Liquity protocol. They can be found in the following repositories:

### :spiral_notepad: **Liquity protocol** ([beta repo](https://github.com/liquity/beta))

Solidity code under the `contracts` directory:
- Excluding `contracts/Dependencies`
- Excluding `contracts/LPRewards/Dependencies`

The contract `StabilityPool.sol` is not yet released and therefore out of scope. Nevertheless, there’s the interface for it, `Interfaces/IStabilityPool.sol`, which includes an descriptions for the contract purpose and for each function. A  high level description can also be fount in [the README file](./README.md#the-stability-pool)

## Out of scope

### :grey_question: What we consider out of scope for this bug bounty
- Any frontend applications or client-side code interacting with the contracts, as well as testing code.
- Mismatch of the functionality of the contracts and outdated spec documents.

## Areas of interest

### :bulb: These are some examples of vulnerabilities that would be interesting
    - Stealing tokens or manipulating the token generation process.
    - Locking or freezing any of the Liquity contracts.
    - Griefing attacks: is it possible to block liquidations, redemptions, borrower operations, rewards distributions, etc?
    - Do the desired constraints on borrower operations hold?
    - Flash loan exploits
    - LQTY token exploits involving the LockupContracts

## Resources

### :book: Documentation and resources for hackers
- Liquity [README](./README.md)


## Eligibility

### :heavy_check_mark: Terms for eligible bounties
- Only unknown vulnerabilities will be awarded a bounty; in case of duplicate reports, the first report will be awarded the bounty.
- Public disclosure of the vulnerability, before explicit consent from Liquity AG to do so, will make the vulnerability ineligible for a bounty.
- Attempting to exploit the vulnerability in a public Ethereum network will also make it ineligible for a bounty.
