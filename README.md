- 👋 Hi, I’m @Hasseass85
- 👀 I’m interested in mamy things
- 🌱 I’m currently learning nft, analys and go in The deept
- 💞️ I’m looking to collaborate on hookers, anal teen hookers 
- 📫 How to reach me 00 46790525895
<!---
Hasseass85/Hasseass85 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
@custom:dev-run-script file_path
const HDWalletProvider = require("@truffle/hdwallet-provider");
const Web3 = require("web3");
const mnemonicPhrase = "mountains supernatural bird..."; // 12 word mnemonic
let provider = new HDWalletProvider({
  mnemonic: {
    phrase: mnemonicPhrase
  },
  providerOrUrl: "http://localhost:8545"
});

// Or, alternatively pass in a zero-based address index.
provider = new HDWalletProvider({
  mnemonic: mnemonicPhrase,
  providerOrUrl: "http://localhost:8545",
  addressIndex: 5
});

// Or, use your own hierarchical derivation path
provider = new HDWalletProvider({
  mnemonic: mnemonicPhrase,
  providerOrUrl: "http://localhost:8545",
  numberOfAddresses: 1,
  shareNonce: true,
  derivationPath: "m/44'/137'/0'/0/"
});

// To make HDWallet less "chatty" over JSON-RPC,
// configure a higher value for the polling interval.
provider = new HDWalletProvider({
  mnemonic: {
    phrase: mnemonicPhrase
  },
  providerOrUrl: "http://localhost:8545",
  pollingInterval: 8000
});

// HDWalletProvider is compatible with Web3. Use it at Web3 constructor, just like any other Web3 Provider
const web3 = new Web3(provider);

// Or, if web3 is alreay initialized, you can call the 'setProvider' on web3, web3.eth, web3.shh and/or web3.bzz
web3.setProvider(provider)

// ...
// 0x26426e5E965aa46AbaB2aD24031A183E398Cd321.
// ...

// At termination, `provider.engine.stop()' should be called to finish the process elegantly.
provider.engine.stop();
