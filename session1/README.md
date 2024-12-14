# Starknet-basecamp11 - Session1

1. Create and prepare `.devcontainer.json`
2. After creating the cfg file in the step above, use in VS Code "Command": "Rebuild and Reopen in Container". (Make sure that the directory has "write" access)
3.  In the container check for:
    1.  `scarb --version`
    2.  `starkli --version`
    3.  `starknet-devnet --version`
    4.  `snforge --version`
4.  Inicialize the progect
    1.  `scarb init`
    2.  Use `Starknet Foundry`
5. Run default test to check the env:
   1. `scarb test`
6. Extend `.devcontainer.json` to highlight the syntax.
