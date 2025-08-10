<h1 align="center">Hey 👋What's Up?</h1>

### About Me

I build secure, scalable DeFi systems using Solidity, Rust, TypeScript, and Python, with a focus on upgradeable smart contracts, clean architecture, and long-term maintainability. My work includes leading the development of mUSD, a Bitcoin-backed stablecoin on Mezo, and Surge-Trade, a Radix-based perpetual DEX with AMM liquidity and front-running protection. With a systems-driven approach, I engineer automated, yield-generating strategies, prioritize test-driven development, and design trustless infrastructure rooted in real utility and sustainable tokenomics.

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=devridge0&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=false" height="150" alt="stats graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=devridge0&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=dracula&hide_border=false" height="150" alt="languages graph"  />
</div>


###

<div align="center">
  <img src="https://github-profile-trophy.vercel.app?username=devridge0&theme=dracula&column=-1&row=1&margin-w=8&margin-h=8&no-bg=false&no-frame=false&order=4" height="150" alt="trophy graph"  />
</div>



### Web3 Auto Transfer Script

```python
from web3 import Web3
import os


# Connect to Ethereum node
w3 = Web3(Web3.HTTPProvider(os.getenv("ETH_NODE_URL")))
assert w3.is_connected(), "Failed to connect"

# Load sender credentials
PRIVATE_KEY = os.getenv("PRIVATE_KEY")
SENDER = w3.eth.account.from_key(PRIVATE_KEY).address
TO = "0xReceiverAddressHere"
AMOUNT = w3.to_wei(0.01, 'ether')

# Build and send transaction
nonce = w3.eth.get_transaction_count(SENDER)
tx = {
    'to': TO,
    'value': AMOUNT,
    'gas': 21000,
    'gasPrice': w3.to_wei('50', 'gwei'),
    'nonce': nonce,
    'chainId': 1
}
signed = w3.eth.account.sign_transaction(tx, PRIVATE_KEY)
tx_hash = w3.eth.send_raw_transaction(signed.rawTransaction)

print("✅ Sent! Tx hash:", tx_hash.hex())
```
<h3>🐟 Fun Fact</h3>

<p align="center">
  <img src="https://github.com/user-attachments/assets/e705e4ed-4efa-4e77-a77b-e29b2980e957" alt="Monkey_developer">
</p>
