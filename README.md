# Foundry Deploy Action

A custom GitHub Action to deploy smart contracts using Foundry. This action automates the process of compiling and deploying your smart contracts to the Ethereum blockchain.

## Features

- Checkout the repository and its submodules.
- Install the Foundry toolchain.
- Set up necessary environment variables.
- Compile smart contracts using Foundry.
- Deploy contracts with optional verification on Etherscan.

## Usage

To use this action in your GitHub workflows, you can add the following YAML snippet to your workflow file:

```yaml
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Foundry Deploy Action
        uses: grossiwm/foundry-deploy-action@v1
        with:
          rpc-url: ${{ secrets.RPC_URL }}
          private-key: ${{ secrets.PRIVATE_KEY }}
          chain-id: 1 # Replace with your desired chain ID
          etherscan-api-key: ${{ secrets.ETHERSCAN_API_KEY }}
          deploy-script: "path/to/your/deploy_script.sol"
```
