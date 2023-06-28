# Swisstronik Early Bird Program (Deploy Smart Contract)


## Referensi

[Dokumen resmi](https://www.swisstronik.com/early-bird-announcement?utm_source=twitter&utm_medium=promo&utm_campaign=EB0623&utm_team=mktld&utm_channel=own_web&utm_creative=0&utm_lang=en&utm_date=jun21)

[Discord](https://discord.com/invite/MsDs3M3uX5)

[Twitter](https://twitter.com/swisstronik)

### STEP 1 : Perbarui sistem

#### 1. Go to : https://remix.ethereum.org

 Klik logo + 

 <p align="center">
 <img height="250" height="auto" src="https://raw.githubusercontent.com/arapzz/Swisstronik_Early/main/Image/Screenshot%202023-06-28%20134618.png">
 </p>

#### 2. Create Workspace 

 Choose a Tamplate : ERC20

 Workspace name : Register

 <p align="center">
 <img height="250" height="auto" src="https://raw.githubusercontent.com/arapzz/Swisstronik_Early/main/Image/Screenshot%202023-06-28%20134649.png">
 </p>

 klik OK

#### 3. Create New File 

<p align="center">
 <img height="250" height="auto" src="https://raw.githubusercontent.com/arapzz/Swisstronik_Early/main/Image/Screenshot%202023-06-28%20134700.png">
 </p>

 ```
 Rename : Register.sol
 ```

<p align="center">
 <img height="250" height="auto" src="https://raw.githubusercontent.com/arapzz/Swisstronik_Early/main/Image/Screenshot%202023-06-28%20134716.png">

 #### 4. Copas Code Edit Github name & your address

 <p align="center">
 <img height="250" height="auto" src="https://raw.githubusercontent.com/arapzz/Swisstronik_Early/main/Image/Screenshot%202023-06-28%20134826.png">

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Register {
string public github;
address public owner;

struct Referral {
    address referralAddress;
    string referralString;
}

Referral[] public referrals;

constructor() {
    github = "GITHUB_USERNAME";
    owner = YOUR_ADDRESS;
}

function addReferral(address _referralAddress, string memory _referralString) external {
    require(msg.sender == owner, "Only the owner can add referrals.");
    referrals.push(Referral(_referralAddress, _referralString));
}

function totalReferrals() public view returns (uint256) {
    return referrals.length;
}
}
```

```
Edit : "GITHUB_USERNAME" and YOUR_ADDRESS
```

### 5. Go to Solidity Compiler and Compile your File

 <p align="center">
 <img height="250" height="auto" src="https://raw.githubusercontent.com/arapzz/Swisstronik_Early/main/Image/Screenshot%202023-06-28%20134826.png">


 Change Compiler Version: v0.8.0+commit.c7dfd78e

 <p align="center">
 <img height="250" height="auto" src="https://raw.githubusercontent.com/arapzz/Swisstronik_Early/main/Image/Screenshot%202023-06-28%20134942.png">

#### 6. Go to Deploy & Run transactions 

 <p align="center">
 <img height="250" height="auto" src="https://raw.githubusercontent.com/arapzz/Swisstronik_Early/main/Image/Screenshot%202023-06-28%20134956.png">

 Change ENVIRONMENT : Injected Provider - Metamask

 <p align="center">
 <img height="250" height="auto" src="https://raw.githubusercontent.com/arapzz/Swisstronik_Early/main/Image/Screenshot%202023-06-28%20135001.png">

 Connect Metamask Wallet and Change Sepolia Test Network 

 <p align="center">
 <img height="250" height="auto" src="https://raw.githubusercontent.com/arapzz/Swisstronik_Early/main/Image/Screenshot%202023-06-28%20135020.png">

 After connect lets klik deploy and confirm transaction

 <p align="center">
 <img height="250" height="auto" src="https://raw.githubusercontent.com/arapzz/Swisstronik_Early/main/Image/Screenshot%202023-06-28%20135030.png">
