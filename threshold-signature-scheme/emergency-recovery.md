---
description: What happens if the TSS software is unavailable
---

# Emergency Recovery

## What is the Emergency Recovery Tool?

In Vultisig the private key never exists, improving the security by timesfold since there is no private key to be extracted or stolen. 

It is possible though to recombine the vault shares of a vault and generate the private key to extract it and use it in other wallets. Scripts are created to allow users to do this if the Vultisig app ever goes offline:

## Prerequisites

* Ensure you have [Go (Golang)](https://golang.org/dl/) installed on your system.

### Option 1: Web UI Version

1.  **Clone the Repository:**

    ```sh
    git clone https://github.com/vultisig/mobile-tss-lib
    ```
2.  **Navigate to the Recovery Web Directory:**

    ```sh
    cd mobile-tss-lib/cmd/recovery-web
    ```
3.  **Run the Web Server:**

    ```sh
    make
    ```

    This command will start the web server, allowing you to access the recovery UI via your web browser.

### Option 2: CLI Version

1.  **Clone the Repository:**

    ```sh
    git clone https://github.com/vultisig/mobile-tss-lib
    ```
2.  **Navigate to the Recovery CLI Directory:**

    ```sh
    cd mobile-tss-lib/cmd/recovery-cli
    ```
3.  **Run the Recovery CLI Tool:**

    ```sh
    go run main.go 
    ```

    Follow the instructions displayed in the terminal to proceed with the recovery process.

{% hint style="danger" %}
Only the following assets are supported; Bitcoin, BitcoinCash, Litecoin, Dogecoin, Ethereum, Thorchain, Mayachain. 

Before the user does this, the private key never existed. This is a one-way function; once the private key is created, the vault is no longer a TSS vault, but a single-signature wallet.

Never use a single-signature wallet again.
{% endhint %}

## Resources

Web: [https://github.com/vultisig/mobile-tss-lib/tree/main/cmd/recovery-web](https://github.com/vultisig/mobile-tss-lib/tree/main/cmd/recovery-web)\
CLI: [https://github.com/vultisig/mobile-tss-lib/tree/main/cmd/cli](https://github.com/vultisig/mobile-tss-lib/tree/main/cmd/cli)
