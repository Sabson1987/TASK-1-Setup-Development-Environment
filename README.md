# TASK-1-Setup-Development-Environment
Set Development Enviroment for Concordium 

Step 1.
Install Rust by typing:
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
then select 1 to Proceed with installation (default)

Step 2.
Install Wasm by typing:
rustup target add wasm32-unknown-unknown

Step 3.
Install Concordium:
- For MacOS:
https://distribution.concordium.software/tools/macos/signed/cargo-concordium_2.7.0

- For Linux:
https://distribution.concordium.software/tools/linux/cargo-concordium_2.7.0

- For Windows:
https://distribution.concordium.software/tools/windows/signed/cargo-concordium_2.7.0.exe

Rename the cargo-concordium-2.7.0 tool to cargo-concordium. The tool should be placed in you PATH.
You can find instruction following the link:
https://developer.concordium.software/en/mainnet/smart-contracts/guides/setup-tools.html#setup-tools

Run command cargo concordium --help to check if everthing is correct. 

Step 4. 
Install Concordium Client 
Download from:
https://developer.concordium.software/en/mainnet/net/installation/downloads-testnet.html#concordium-node-and-client-download-testnet

Once downloaded, install the package. Then in Terminal go to the folder where you downloaded the concordium-client and execute by:
 chmod +x concordium-client ( for Linux/MacOS)
 
Check and connect to test node.

Check:
concordium-client -help

Connect to test node:
concordium-client consensus status --grpc-port 10000 --grpc-ip node.testnet.concordium.com

Step 5.
Setup a wallet

Use the link to install a Concordium Wallet:
https://chrome.google.com/webstore/detail/concordium-wallet/mnnkpffndmickbiakofclnpoiajlegmg?hl=en-US

Follow the instructions to open new Account for Concordium testnet IP.
Once you setup new account , under Account tab go to settings (located in the bottom right corner ) , then input for passcode and press EXPORT.

Then import the key in your Terminal:
using command:
concordium-client config account import <YOUR PUBLIC ADDRESS.export> --name <Your-Wallet-Name>

where <YOUR PUBLIC ADDRESS.export> is a file name and <Your-Wallet-Name> is your concordium wallet account. 
