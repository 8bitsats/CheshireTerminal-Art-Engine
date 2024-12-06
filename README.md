# NFT Generation Client

A powerful NFT generation system that combines AI art generation with Solana NFT minting. This client uses a local Flux model for image generation and Metaplex for NFT creation.

## Features

- 🎨 AI Art Generation using local Flux model
- 🤖 AI-powered prompt generation using LM Studio
- 🖼️ NFT minting on Solana using Metaplex
- 💎 Helius RPC integration for reliable network access
- 🎭 Character-driven art generation with AI Artist personality

## Prerequisites

- Node.js >= 16.0.0
- Python 3.10 or higher with the Flux model setup
- LM Studio running locally
- Solana CLI tools
- A Solana wallet with SOL for transactions

## Setup

1. Install dependencies:
   ```bash
   npm install
   ```

2. Copy the environment template and fill in your values:
   ```bash
   cp .env.template .env
   ```

3. Configure your environment variables in `.env`:
   - Add your Helius RPC URL
   - Set your wallet private key
   - Configure LM Studio URL
   - Set other NFT-related parameters

4. Ensure the Flux model is properly set up in the ArtEngine directory:
   ```
   ArtEngine/
   ├── model/
   │   └── flux1-dev.safetensors
   └── fluxclient.py
   ```

## Usage

### Generate and Mint a Single NFT

```bash
npm run generate
```

This will:
1. Generate an AI-powered artistic prompt
2. Create unique artwork using the Flux model
3. Upload the artwork to Arweave
4. Mint an NFT on Solana
5. Return the NFT details and metadata

### Run Tests

```bash
npm test
```

## Architecture

The system consists of several key components:

1. **NFT Generation Client** (`nft-client.js`)
   - Main interface for NFT generation and minting
   - Handles Metaplex integration
   - Manages metadata creation

2. **AI Art Generation** (`fluxclient.py`)
   - Local Flux model for image generation
   - High-quality art generation
   - Customizable parameters

3. **Prompt Generation** (LM Studio)
   - AI-powered prompt creation
   - Character-driven creativity
   - Philosophical and artistic themes

4. **Blockchain Integration**
   - Solana network interaction
   - Metaplex NFT standard
   - Helius RPC for reliable access

## File Structure

```
client/
├── nft-client.js         # Main NFT generation client
├── test-nft-generation.js # Test suite
├── package.json          # Dependencies and scripts
├── .env.template         # Environment variable template
└── README.md            # Documentation
```

## Environment Variables

| Variable | Description | Example |
|----------|-------------|---------|
| HELIUS_RPC_URL | Helius RPC endpoint | https://rpc-devnet.helius.xyz/?api-key=YOUR_KEY |
| WALLET_PRIVATE_KEY | Wallet private key array | ["key", "array"] |
| SOLANA_NETWORK | Solana network to use | devnet |
| LM_STUDIO_URL | Local LM Studio URL | http://192.168.1.170:1234 |
| COLLECTION_NAME | NFT collection name | "AI Generated Art" |
| COLLECTION_SYMBOL | Collection symbol | "AIGEN" |

## Error Handling

The client includes comprehensive error handling for:
- Image generation failures
- Network connectivity issues
- Blockchain transaction errors
- Metadata upload problems

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

MIT License - feel free to use this code for your own projects!
