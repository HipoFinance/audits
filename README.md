# Hipo Protocol Audits

## 2023-10 [TonTech](https://ton.tech/) Hipo Audit Report

The team reported a total of 5 issues:

- Low Risk Issues: 4 (2 Resolved)
- Informational Issues: 1 (1 Resolved)

See [full report](TonTech%20Hipo%20Audit%20Report%202023-10.pdf) for more details.

### Unresolved Issues

- **Missing late participation check**: There is a check for late participation and even in the case of a network stop and restart after the participation time, there will be no harm to the protocol, only borrowers will skip that round.

- **Missing sender checks**: To make the protocol permission-less, the `stake_coins` and `withdraw_tokens` messages can be sent by anyone willing to pay the gas fee. Usually the driver will send these messages, but anyone can also send these, so in case the driver stops working, users can withdraw their funds.
