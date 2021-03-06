# Xenophyte-Desktop-Wallet

This is the official Xenophyte Desktop Wallet compatible with Netframework 4.6.1 minimum or Mono.

**In production, we suggest compiling the wallet in Release Mode for disabling log files.**


Windows:

- Visual Studio is required.
- NetFramework 4.6.1 or newer (https://dotnet.microsoft.com/download/dotnet-framework/)
- Compilation Flags: WINDOWS-DEBUG, WINDOWS-RELEASE  or LINUX-DEBUG, LINUX-RELEASE

Linux:

- Mono Framework (https://www.mono-project.com/)

- For compile the project Mono is required, you can also compile the project with Visual Studio and make a Linux Binary, remember to use LINUX-DEBUG or LINUX-RELEASE (for production) compilation flags.

For make a binary linux file from executable windows file:

~~~~text
mkbundle --list-targets // Give the list of all target runtime
~~~~ 

Example of target: 4.6.1-linux-libc2.12-amd64

~~~text
mkbundle --fetch-target 4.6.1-linux-libc2.12-amd64 // Functional for Ubuntu 18.04 64bits

mkbundle --cross 4.6.1-linux-libc2.12-amd64 Xenophyte-Desktop-Wallet.exe -o Xenophyte-Desktop-Wallet Xenophyte-Connector-All.dll  MetroFramework.dll zxing.dll  --deps -z --static
~~~

Informations:

- Xenophyte Desktop Wallet gui provide the possibility to get your current balance without to be sync at 100%.

- You can send/receive transaction without to be sync at 100%.

- The wallet gui will always sync accurate transaction informations, he will never ask the whole transaction data of the network, only yours.

- Some options of sync, can be help you to choose the right one, you can use by default seed nodes for sync your wallet or you can use the public list of remote node and seed nodes together. You can also use your own private remote node , this option is only recommended once you select your own remote node. 

- The wallet gui will always contact seed nodes for check every informations provided by remote nodes listed on the public list of them before to use them.

- The pin code asked by the blockchain can be disabled, this option is independent for each wallet.

- Remember to save somewhere your wallet informations: private key, public key, pin code just in case.

- The Xenophyte network don't allow multiple connections on the same wallet. 

- The Xenophyte network provide to your wallet gui an approximative time of receive when you try to send a transaction.

- Every information what you get on your transaction history cannot be read by another wallet

For more informations about how work the network connection of wallet, please check the WhitePaper of Xenophyte.

**Be sure to compile in release mode those source for don't enable Log System of the wallet**

**Xenophyte-Connector-All Library is required for compile the gui wallet: https://github.com/Xenophyte-coin/Xenophyte-Connector-All**

**Developers:**

- Xenophyte

**Language files contributors:**

- English: Xenophyte, DigitalTwister, AlpHA

- French: Xenophyte

- German: Stone

- Greek: Alpha

- Hungarian: Maxy86

- Polish: XenophyteEnthusiast

- Chinese: bobolam1971

**Official testers:**

- DigitalTwister
- Sniperviperman
- AlpHA
- Maxy86
- Wolfierawr
- Rashed
- Sabrar
- Xenophyte
- PhelanConaill

**External library used: MetroFramework (used on Windows only) a good UI, fast and provide less freezing: https://github.com/dennismagno/metroframework-modern-ui**

**--> Use this one: https://github.com/Xenophyte/metroframework-modern-ui**

**External library used: ZXing.Net, a QR Code generator used since version 0.4.8.7R: https://github.com/micjahn/ZXing.Net/**

**Newtonsoft.Json library is used since version 0.7.0.0R for the Token Network mode system: https://github.com/JamesNK/Newtonsoft.Json**
