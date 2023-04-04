# jetton-dao-contracts

## Testnet env

[Testnet](https://dao-viewer-testnet-v2.vercel.app)

[First DAO](https://dao-viewer-testnet-v2.vercel.app/EQCA_CvplU57Pk4mhXJZmZYcf-SfhI-IIV1BStAXXoaNu-sN/)


## unit-tests

```
> jest --verbose

 PASS  tests/VoteKeeper.spec.ts
  VoteKeeper
    ✓ should deploy and proxy vote (624 ms)
    ✓ should proxy additional second vote (360 ms)
    ✓ should fail additional second vote, because not enough weight  (527 ms)
    ✓ should fail vote keeper deploy, because of wrong deployer (263 ms)

 PASS  tests/InitDao.spec.ts (5.153 s)
  DaoCollection
    ✓ should create init transaction and deploy jetton (639 ms)
    ✓ should fail init transaction, because already activated (377 ms)

 PASS  tests/NftProposal.spec.ts (6.022 s)
  NftProposal
    ✓ should fail on deploy nft proposal, because of wrong deployer (542 ms)
    ✓ should deploy nft proposal (337 ms)
    ✓ should fail on execute, because not enough funding (307 ms)
    ✓ should execute proposal (288 ms)
    ✓ should fail on execute, because of double execute (294 ms)
    ✓ should fail on execute, because of expiration date (292 ms)

 PASS  tests/Deployer.spec.ts (7.408 s)
  Deployer
    ✓ should deploy (552 ms)
    ✓ should update price (255 ms)
    ✓ should update price and royalty (341 ms)
    ✓ should not update price (244 ms)
    ✓ should update codes (221 ms)
    ✓ should not update codes (232 ms)
    ✓ should update admin address (279 ms)
    ✓ should fail on updating admin address (250 ms)
    ✓ should withdraw tons (204 ms)
    ✓ should send withdraw jetton message (228 ms)
    ✓ should fail on mint data because of price (250 ms)
    ✓ should mint dao (277 ms)

 PASS  tests/JettonWallet.spec.ts (8.83 s)
  JettonWallet
    ✓ should deploy with correct balance (428 ms)
    ✓ should deploy with correct addresses (436 ms)
    ✓ should send vote and deploy voteKeeper (317 ms)
    ✓ should have 0 available balance after voting (314 ms)
    ✓ should have all locked balance after voting (278 ms)
    ✓ should fail vote, because of expiration date too high (297 ms)
    ✓ should fail vote, because of voting already finished (251 ms)
    ✓ jetton wallet should send burn message (263 ms)
    ✓ jetton wallet should fail burn message, because of owner (286 ms)
    ✓ jetton wallet should send jettons (311 ms)
    ✓ jetton wallet should fail send jettons, because of owner (284 ms)
    ✓ can not send to masterchain (220 ms)
    ✓ owner can withdraw excesses (252 ms)
    ✓ not owner can not withdraw excesses (307 ms)
    ✓ owner can withdraw jettons owned by JettonWallet (409 ms)
    ✓ not owner can not withdraw jettons owned by JettonWallet (369 ms)

 PASS  tests/DeployedDao.spec.ts (11.838 s)
  DeployedDao
    ✓ should get jetton data (601 ms)
    ✓ should get collection data (323 ms)
    ✓ should mint proposal and increment proposal index (354 ms)
    ✓ should mint 5 proposal and increment proposal index (549 ms)
    ✓ should have the same jetton minter addresses (319 ms)
    ✓ impossible to send too much jettons (378 ms)
    ✓ malformed forward payload (306 ms)
    ✓ correctly sends forward_payload (406 ms)
    ✓ no forward_ton_amount - no forward (429 ms)
    ✓ check revert on not enough tons for forward (377 ms)
    ✓ works with minimal ton amount (434 ms)
    ✓ wallet does not accept internal_transfer not from wallet (330 ms)
    ✓ wallet owner should be able to burn jettons (392 ms)
    ✓ not wallet owner should not be able to burn jettons (371 ms)
    ✓ wallet owner can not burn more jettons than it has (348 ms)
    ✓ minimal burn message fee (393 ms)
    ✓ minter should only accept burn messages from jetton wallets (294 ms)
    ✓ report correct discovery address (403 ms)
    ✓ Minimal discovery fee (341 ms)
    ✓ Correctly handles not valid address in discovery (302 ms)

 PASS  tests/DaoFlow.spec.ts (28.389 s)
  DaoFlow
    ✓ dao should mint tokens and increment total supply (4400 ms)
    ✓ dao should send tons (4111 ms)
    ✓ create nft proposal, transfer jetton to dao, execute proposal and transfer jetton to second user (4260 ms)
    ✓ should create nft proposal, transfer nft to dao, execute proposal and by it transfer nft to second user (4191 ms)
    ✓ dao should update content (4095 ms)
    ✓ dao should update quorum (4079 ms)

Test Suites: 7 passed, 7 total
Tests:       66 passed, 66 total
Snapshots:   0 total
Time:        28.568 s, estimated 30 s
Ran all test suites.
```