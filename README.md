# Hotel 2000
## Instalation
1) Instalation de la blockchaine <br>
    ``` bash
    sudo bash ./scripts/install.sh
    ./scripts/create-blockchain.sh
    ```
2) Build solidity contract (to java contract) <br>
    `mvn web3j:generate-sources`
3) Maven clean install <br>
    `mvn clean install`
4) Creation d'un compt pour deployer le/les contract(s) <br>
<br>
    Lancer le script `./scripts/create-count.sh <YOUR_PASSWORD> deploy` pour générer un compt <br>
    Exemple: `./scripts/create-count.sh azerty deploy`<br>
    <br>
    Pour deployer deployer le/les contract(s) l'utilisteur a besoin d'argant. <br>
    Pour cela il est possible de miner avec le script mine.sh par exemple: `./scripts/mine.sh ab9f2020e56dbae3a2d7d0eefaff5df7fba0a7cc`  

## Build/Run
1) Build solidity contract (to java contract) <br>
    `mvn web3j:generate-sources` <br>
2) Run Ethereum server <br>
    `./scripts/server.sh` <br>
    Ce script mine de Ethereum pour ajouter des transation/contract a la blockchain. <br>
    Il est possible de miner pour un utilisateur specifique exemple: <br>
    `./scripts/server.sh ab9f2020e56dbae3a2d7d0eefaff5df7fba0a7cc` <br>
3) Build and run App.java