## Introduction
<p>
What is cryptocurrency?
Cryptocurrency can be defined as a digital currency that positions as an alternative form of payment created using encryption algorithms.

How is it related to DEX?
A DEX provides a peer to peer marketplace where  crypto traders undertake transactions among themselves directly. DEXs fulfill one of cryto's core possibilities: fostering financial transactions that are NOT officiated by any intermediary.
<p>
<p>
Simply put, a DEX is a trading platform that operates without a central authority. Instead of a company managing your trades and holding your assets, a DEX allows you to trade cryptocurrencies directly with other users through a decentralized network.
Think of a DEX like a farmers’ market where buyers and sellers meet directly. There’s no middleman; instead, you interact with the other party through a marketplace that facilitates the transaction.
</p>

## How to buy/store crypto?
<p>
    fees for buying crypto depends on the payment method and platform used.
    1. crypto currency wallet apps(e.g. Bitcoin.com) 
    2. Brokerage(an intermediary that facilitates buying and selling of cryptocurrencies for retail investors)(e.g. Etoro)
    3. CEX
    4. Peer to peer exchange platforms(e.g. peach bitcoin)
</p>

#### centralized exchange
<p>
    CEXs in DeFi space are online trading platforms that are typically owned and operated by private companies. 
    For e.g. Binance, Coinbase, WizarX. 
    Let's explore some drawbacks of CEX:
        1. Exchange can flee with FTX
        2. govt. can ask the exchange to block.
        3. privacy concerns
        3.1 CEXs are very prone to cyberattacks and hacks
        3.2 exit scam - cryto exchanges claim to have lost all private keys and control over assets

        To overcome these, DEXs have handed the owmnership of the assets to the user.
</p>

#### cold storage
<p>
    Cold wallet, also known as a cold storage wallet, is a type of cryptocurrency wallet that is not connected to the internet. Cold wallets are used to store the private keys of a user's cryptocurrency offline, in order to protect them from hacking and other online threats.
</p>

## CEX v/s DEX
<p>
    points | CEX | DEX |
    -- | -- | -- |
    Basis of trading | centralized intermediary | peer to peer(users and liquidity providers)
    KYC | must needed | May be overlooked
    Security concerns | vulnerable to attacks | secured and backed by blockchain and smart contracts
    convenience | user-friendly | may seem complicated to new users
    private keys | owned by central authority | kept by users
    tokens | limited options | farmore options
    impermanent loss | no such concerns due to hgh liquidity | high risk during market fluctuations
    trading options | many options(future trading, spot trading etc.) | limited options(crypto lending, invesment options)
</p>

## Why do we need a DEX?
<p>
    The idea behind a DEX is "disintermediation," which means removing middlemen to allow regular people to do business directly with each another. A DEX doesn't offer custody of users’ crypto assets. Instead, users directly hold all their assets in their own wallets at all times.
    Decentralized crypto exchanges (DEXs) are blockchain-based apps that coordinate large-scale trading of crypto assets between many users. They do that entirely through automated algorithms, instead of the conventional approach of acting as financial intermediary between buyers and sellers.
    Some DEXs are Uniswap, Ethereum, Sushiswap, BNB etc.
    
</p>
<p>
    why liquidity pools?
    liquidity refers to the ability to buy or sell your assets quickly without significant fluctuations in price.
    DEXs suffer from high market volatility since liquidity depends heavily on the number of actively trading users on the platform.
    hence DeFi space has liquidity pools as a solution.(add a visual of how liquidity pool solves it)
</p>

## How to build a DEX?
<p>
    Let's build a simple liquidity pool in solidity.

    1. first 
    2. This <strong>LiquidityPool</strong> contract allows for the creation and management of a liquidity pool for an ERC-20 token. It enables the exchange of ETH for tokens and vice versa, and allows the owner to add or remove liquidity from the pool.
    (add code lines 7-14)
    3. The <strong>initializePool</strong> function initializes the liquidity pool with a specific amount of tokens and ETH. It can only be called by the owner and ensures the pool is not already initialized and the amounts are valid.
    (code lines 16-23)
    4. Then we define <strong>getPrice</strong> function  to calculate the output amount based on input amount, reserves, and a fee. It uses the constant product formula  of AMM with a 0.3% fee.
    (code lines 25-30)
    5. The <strong>ethToToken</strong> function swaps ETH for tokens and calculates the amount of tokens to send based on the amount of ETH sent and the current reserves. Then it updates the liquidity reserves accordingly.
    (code lines 32-42).
    6. After that we have the <strong>tokenToEth</strong> function to swap the tokens back for ETH and updates the pool accordingly.
    (code lines 44-55).
    7. Then <strong>addLiquidity</strong> function allows the owner to add more liquidity to the pool and increases both token and ETH reserves.
    (code lines 57-63).
    8. And the <strong>removeLiquidity</strong> function removes the liquidity from the reserves.
    (code lines 65-74).
</p>



## Recap
<p>
    1. Crypto: Digital currency secured by cryptography, used for transactions.
    2. DEX: Decentralized trading platform, no central authority, direct user-to-user transactions.
    3. Then we discussed how to buy and store crypto.
    4. Comparison between CEX and DEX
    5. We discussed why there's a need for DEX.
    6. We built a simple DEX in node.js and express.
</p>