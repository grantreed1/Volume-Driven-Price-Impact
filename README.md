# Estimating Market Impact From Position Accumulation
We investigate the temporary price impact $I(V)$ of trade volume $V$ across cryptocurrency markets, specifically focusing on Ethereum (ETH) and Solana (SOL). We aim to determine how well crypto markets absorb large block trades without moving the price. 

## Square Root Law of Market Impact vs. Empirical Power Law
We model the temporary price impact against executed volume. We evaluate two distinct models:

1. **The Square Root Law (Theoretical):** The industry-standard baseline which assumes price impact scales with the square root of volume: 
   $$I(V) \propto V^{0.5}$$
2. **The Power Law Fit (Empirical):** A data-driven model designed to capture the actual observed concavity in the limit order book:
   $$I(V) \propto V^{\mu_2}$$

## Key Findings:
Empirical evidence from both Ethereum and Solana datasets confirms a structural departure from the theoretical Square Root Law. While both assets exhibit extreme concavity, their liquidity profiles and absorption capacities differ significantly.

### 1. Solana (SOL): 
* Solana demonstrates a substantially more stable and cleaner statistical fit to the empirical Power Law.
* However, its limit order book is approximately **3.4 times more sensitive** to trade volume than Ethereum, resulting in higher execution friction for large block trades.

### 2. Ethereum (ETH):
* Ethereum exhibits a near-zero exponent for its Power Law fit ($\mu_2 \approx 0$).
* This structural concavity suggests a massive level of top-of-book depth, allowing the ETH market to absorb institutional sweeps and large position accumulations with far less price friction than Solana.

### Data Notice: 
> The high-frequency tick and order book data used to model the empirical Power Law fits are stored in massive .parquet files that exceed GitHub's repository limits.
