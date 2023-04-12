# jetton-dao-contracts

## Testnet env

[Testnet](https://dao-viewer-testnet-v2.vercel.app)

[First DAO](https://dao-viewer-testnet-v2.vercel.app/EQCFSH3MUnhUPdxU9XZ2L16A6D71zbrL7K3dcsJkodGKxaNw/)


## unit-tests

```
> jetton-dao@0.0.1 test
> jest --verbose

 PASS  tests/VoteKeeper.spec.ts
  VoteKeeper
    ✓ should deploy and proxy vote (1068 ms)
    ✓ should proxy additional second vote (393 ms)
    ✓ should fail additional second vote, because not enough weight  (490 ms)
    ✓ should fail vote keeper deploy, because of wrong deployer (316 ms)

 PASS  tests/InitDao.spec.ts
  DaoCollection
    ✓ should create init transaction and deploy jetton (627 ms)
    ✓ should fail init transaction, because already activated (346 ms)

 PASS  tests/NftProposal.spec.ts (5.711 s)
  NftProposal
    ✓ should fail on deploy nft proposal, because of wrong deployer (477 ms)
    ✓ should deploy nft proposal (438 ms)
    ✓ should fail on execute, because not enough funding (311 ms)
    ✓ should execute proposal (297 ms)
    ✓ should fail on execute, because of double execute (365 ms)
    ✓ should fail on execute, because of expiration date (294 ms)

 PASS  tests/Deployer.spec.ts (7.172 s)
  Deployer
    ✓ should deploy (520 ms)
    ✓ should update price (298 ms)
    ✓ should update price and royalty (301 ms)
    ✓ should not update price (253 ms)
    ✓ should update codes (281 ms)
    ✓ should not update codes (242 ms)
    ✓ should update admin address (296 ms)
    ✓ should fail on updating admin address (244 ms)
    ✓ should withdraw tons (200 ms)
    ✓ should send withdraw jetton message (244 ms)
    ✓ should fail on mint data because of price (217 ms)
    ✓ should mint dao (274 ms)

 PASS  tests/JettonWallet.spec.ts (8.404 s)
  JettonWallet
    ✓ should deploy with correct balance (411 ms)
    ✓ should deploy with correct addresses (452 ms)
    ✓ should send vote and deploy voteKeeper (325 ms)
    ✓ should have 0 available balance after voting (306 ms)
    ✓ should have all locked balance after voting (288 ms)
    ✓ should fail vote, because of expiration date too high (335 ms)
    ✓ should fail vote, because of voting already finished (254 ms)
    ✓ jetton wallet should send burn message (277 ms)
    ✓ jetton wallet should fail burn message, because of owner (280 ms)
    ✓ jetton wallet should send jettons (304 ms)
    ✓ jetton wallet should fail send jettons, because of owner (280 ms)
    ✓ can not send to masterchain (214 ms)
    ✓ owner can withdraw excesses (252 ms)
    ✓ not owner can not withdraw excesses (306 ms)
    ✓ owner can withdraw jettons owned by JettonWallet (409 ms)
    ✓ not owner can not withdraw jettons owned by JettonWallet (367 ms)

 PASS  tests/DeployedDao.spec.ts (13.734 s)
  DeployedDao
    ✓ should get jetton data (629 ms)
    ✓ should get collection data (363 ms)
    ✓ should mint proposal and increment proposal index (392 ms)
    ✓ should mint 5 proposal and increment proposal index (671 ms)
    ✓ should have the same jetton minter addresses (337 ms)
    ✓ impossible to send too much jettons (411 ms)
    ✓ malformed forward payload (333 ms)
    ✓ correctly sends forward_payload (454 ms)
    ✓ no forward_ton_amount - no forward (474 ms)
    ✓ check revert on not enough tons for forward (419 ms)
    ✓ works with minimal ton amount (497 ms)
    ✓ wallet does not accept internal_transfer not from wallet (342 ms)
    ✓ wallet owner should be able to burn jettons (425 ms)
    ✓ not wallet owner should not be able to burn jettons (408 ms)
    ✓ wallet owner can not burn more jettons than it has (384 ms)
    ✓ minimal burn message fee (435 ms)
    ✓ minter should only accept burn messages from jetton wallets (323 ms)
    ✓ report correct discovery address (433 ms)
    ✓ Minimal discovery fee (350 ms)
    ✓ Correctly handles not valid address in discovery (338 ms)
    ✓ dao should handle process test message (340 ms)
    ✓ dao should handle process excesses message (311 ms)
    ✓ dao should handle process assign nft message (304 ms)
    ✓ dao should handle process transfer jetton message (309 ms)
    ✓ dao should handle process empty non bounce message (331 ms)

 PASS  tests/DaoFlow.spec.ts (61.234 s)
  DaoFlow
    ✓ dao should mint tokens and increment total supply (4354 ms)
    ✓ dao should mint tokens for 4 accounts and increment total supply (4473 ms)
    ✓ dao should send tons (4139 ms)
    ✓ dao should mint tokens and send ton in one proposal (4223 ms)
    ✓ create nft proposal, transfer jetton to dao, execute proposal and transfer jetton to second user (4272 ms)
    ✓ should create nft proposal, transfer nft to dao, execute proposal and by it transfer nft to second user (4190 ms)
    ✓ dao should update content (4080 ms)
    ✓ dao should update quorum (4113 ms)
    ✓ dao should not update quorum, because vote result against (4074 ms)
    ✓ dao should not update quorum, because vote result is equal (8036 ms)
    ✓ dao should not update quorum, because vote result not match quorum (11755 ms)

Test Suites: 7 passed, 7 total
Tests:       76 passed, 76 total
Snapshots:   0 total
Time:        61.449 s
Ran all test suites.
```