# Starknet-basecamp11 - Session2

1. Use `.devcontainer.json` srom `session1`
2. Clean `lib.cairo` and create `counter` folder in `src` and `counter.cairo` in `counter` folder
3. Fill `lib.cairo` and `counter.cairo`
4. Template for `lib.cairo` to modify: https://gist.github.com/okhaimie-dev/38af1ffdeaa7f9728354dd6dcb4ae90c
5. extend step 4 with Emit events: https://book.cairo-lang.org/ch14-03-contract-events.html
6. Use external contracts and libraries scarbs.xyz 
  - install `scarb add openzeppelin_access@0.20.0`
  - extend lib.cairo with `ownable` https://docs.openzeppelin.com/contracts-cairo/0.20.0/access
7. deploy contract 
  - create keystore: `starkli signer keystore new keystore.json` 
  - create account: `starkli account oz init account.json --keystore keystore.json`
  - top up the contract from the command above on sepolia network 0.01 ETH
  - upload: `starkli account deploy account.json --keystore keystore.json`
  - declare the contract: `starkli declare target/dev/Counter.contract_class.json --account account.json --keystore keystore.json`
  - deploy: `starkli deploy DECLARED_HASH_FROM_PREVIOUS_STEP INITIAL_VALUE YOUR_WALLET_PUB_ADDRESS --account account.json --keystore keystore.json` 
8. Check the contract on https://sepolia.starkscan.co/contract/
 - use read/write tabs to play with it
