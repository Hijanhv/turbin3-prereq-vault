# pre-req-vault

Turbin3 Q4 2026 prerequisite, Part 1.

- Starter code: [ShrinathNR/pre-req-vault](https://github.com/ShrinathNR/pre-req-vault). My changes are the commits after `f9f7ff7`.
- Change: `withdraw` now does a CPI to the Turbin3 registration program with my GitHub username (`Hijanhv`).
- Video: https://youtu.be/3qmsAns-KWE

![Architecture](docs/architecture.png)

## Devnet

- Vault program: [`73YEzwcbwhygse5vFX7LH1spxMngPwugWk5U3Ye8D981`](https://explorer.solana.com/address/73YEzwcbwhygse5vFX7LH1spxMngPwugWk5U3Ye8D981?cluster=devnet)
- Registration account: [`49M2kvPcWHYhS11vLowwPQ8bRchZyKXKExTpJMzGJPhA`](https://explorer.solana.com/address/49M2kvPcWHYhS11vLowwPQ8bRchZyKXKExTpJMzGJPhA?cluster=devnet)
- Withdraw tx with the CPI: [`4nt4gtER...`](https://explorer.solana.com/tx/4nt4gtEREfB1xVMUUb736wt3dfp1efYo1ScuQg3jCiXsJQUmVtCZmEhNpoTh5rhnK1mXWmnMdCcsxLZdtPFqkAdZ?cluster=devnet)

## Run

```
anchor build
solana program deploy target/deploy/pre_req_vault.so --program-id target/deploy/pre_req_vault-keypair.json
anchor test --skip-build --skip-deploy
```

- Test amounts lowered to 0.2 SOL deposit / 0.1 SOL withdraw (faucet was rate limited).
