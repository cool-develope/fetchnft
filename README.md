# Fetch-NFT

## Subgraph Studio

The subgraph studio url: https://thegraph.com/studio/
First, need to connect the wallet, and then create the project with github repo url. The commands are as follows:

```bash
# install graph-cli
npm install -g @graphprotocol/graph-cli@0.20.1

# authenticate the legacy explorer
graph auth --product hosted-service https://api.thegraph.com/deploy/ <ACCESS TOKEN>

cd fetch-nft
graph codegen subgraph.yaml
graph build subgraph.yaml 

graph deploy  --product hosted-service --ipfs https://api.thegraph.com/ipfs/ --node https://api.thegraph.com/deploy/ <GITHUB_USER/SUBGRAPH_NAME>
```