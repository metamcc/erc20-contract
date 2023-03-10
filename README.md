# MyCreditChain(MCC) Token

MyCreditChain(MCC) is a blockchain platform of personal credit information. This project aims to bring the ownership of credit information back to individuals. MCC revolutionizes the all process of how personal credit information is gathered and used. Moreover, MCC can further revolutionize our interaction with one another in one global network. 

# Smart Contract


- ## MCCToken
    - MCCToken is based on ERC20 standard.
    - To prevent overflow with arithmetic operations, MCCToken uses SafeMath library
    - MCCToken has functionalities for token distribution and blocking token transfer handled by Crowdsale contract
    - Blocking token transfer that locks MCC token of specific token owener is added to prevent unfortunate accident like hacking
    - MCCToken contract also applies "MultiOwnable" to prevent that fund is abused by a specified person
    - MCCToken defines the token standard will be used for MCC service

    - Public Variables:

        1. **name**     - token name   (ERC20 option)
        2. **symbol**   - token symbol (ERC20 option)
        3. **decimals** - number of digits the cryptocurrency has after the decimal point (ERC20 option)

    - Functions:

        1. **issue(address _to, uint256 _value) external  onlyOwner canIssue** - CCToken can not issue but it need to distribute tokens to contributors while crowding sales. So. we changed this Issue tokens to specified wallet
        2. **destroy(address _from, uint256 _value) external** - Destroy tokens on specified address (Called by owner or token holder). Fund contract address must be in the list of owners to recall token during refund
        3. **increaseApproval(address _spender, uint _addedValue) public returns (bool)** - Increase the amount of tokens that an owner allowed to a spender. approve should be called when allowed[_spender] == 0. To increment allowed value is better to use this function to avoid 2 calls (and wait until the first transaction is mined)
        4. **decreaseApproval(address _spender, uint _subtractedValue) public returns (bool)** - Decrease the amount of tokens that an owner allowed to a spender. approve should be called when allowed[_spender] == 0. To decrement allowed value is better to use this function to avoid 2 calls (and wait until the first transaction is mined)


# Future Plans
![Alt text](https://www.mycreditchain.org/images/mcc-eco.png "MCC ECO SYSTEM")

The services provided by MyCreditChain can be summarized as follows.

- The B2P credit information transaction is expected to be the most active within the MCC network. MyCreditChain provides a platform for individuals and companies to make direct transaction of information.

- In the MCC network, individuals can start a P2P financing business. Its platform can be used to make and exchange contracts for private transactions between individuals. With mutual consents, each party can look through other party???s credit information to identify reliability.

- Individuals can submit various official documents online when they apply for services from financial institutions.

- In the MCC network, non-financial data(Alternative Data) can be used for the credit evaluations, thus giving open chances for those who lack proper financial information.
