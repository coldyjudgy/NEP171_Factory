# NEP171_Factory

## About NEP171_Factory
NEP171_Factory allows you to mint standard NFT(Non-Fungible-Token) of [NEAR-Protocol](https://github.com/near/NEPs/blob/ea409f07f8/specs/Standards/NonFungibleToken/Core.md).

## Getting Started
Clone this repository

```jsx
git clone https://github.com/kwklly/NEP171_Factory
cd NEP171_Factory
```

Compile Contract code

```jsx
cargo build --target wasm32-unknown-unknown --release
```

Login
```jsx
near login
```

Deploy Contract

```jsx
near deploy --wasmFile target/wasm32-unknown-unknown/release/non-fungible-token.wasm --accountId YOUR_ACCOUNT
```

Init Contract

```jsx
near call YOUR_ACCOUNT new '{"owner_id":"OWNER_ACCOUNT", "metadata":{"spec":"nft-1.0.0", "name": "nft-1", "symbol": "ANY_SYMBOL"}}' --accountId YOUR_ACCOUNT
```

Mint NFTs
```jsx
near call YOUR_ACCOUNT nft_mint '{"token_id":"TOKEN_ID", "token_owner_id":"OWNER_ACCOUNT", "token_metadata":{"title":"TOKEN_TITLE", "media" : "YOUR_MEDIA" }}' --accountId YOUR_ACCOUNT --depositYocto 6380000000000000000000
```
- [how to customize your metadata](https://github.com/near/NEPs/blob/ea409f07f8/specs/Standards/NonFungibleToken/Metadata.md#interface)
- ``depositYocto`` can increase
