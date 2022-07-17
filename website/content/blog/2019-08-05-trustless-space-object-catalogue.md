+++
title = "An open, borderless, decentralised, trustless space object catalogue. Possible or wishful thinking?"
date = 2019-08-05
[taxonomies]
tags=[]
+++

A real problem in the space situational awareness community, is the lack of a shared validated catalogue of known space debris. This holds back progress in a wide range of areas from operations to fundamental research.

Could an open, borderless, decentralised, trusteless space object catalogue be the solution? If so, how could one ensure the catalogue was tamper proof?

For an entirely open ledger of space debris objects to work, it must operate in a trustless environment. It has to be resistant from malicious actors wanting to delete, edit or provide false entries. What is needed is a mechanism for reaching a global decentralized consensus.

One solution is using the concept of ‘proof of work’. This mechanism achieves consensus without a central trusted authority and provides security through an investment of energy. A person who joins the network must do some amount of computational work to maintain the space object catalogue (e.g. calculation of orbit determination/prediction and orbit validation). The results are stored in a ‘block’ containing information. To do this costs energy in the form of electricity used by the computer. If a submitted block satisfies some pre-agreed criteria a solution is found and the participant is rewarded in some way.

Finding a valid block if found when the participant in the network successfully solves a mathematical challenge which has an adjustable level of difficulty, ensuring that a solution is on average found at regular time intervals (allowing for the solution to propagate the network). Each participant in the network is competing to find a valid block. The larger the computational power a participant uses, the larger the probability of finding a valid block is. The combined energy use amongst the participants hoping to find a valid block becomes ever larger as more people join the competition on the network.

The result of the work is a valid block of data (containing information about the pieces of debris) and is easily verified and subsequently appended to a chain of other blocks, known as a blockchain. If somebody wishes to change the data stored on the blockchain, they must outperform the computational power of the entire network and be able to sustain this computational power. To make a change to a block further down the blockchain requires an enormous amount of computational power as all subsequent blocks will have to be re-computed. For a block far enough down the chain recomputing it and all subsequent blocks becomes impossible.

In this way, the integrity of the catalogue is secured thermodynamically, as there is only so much energy available for computing. A catalogue of space debris data can thus be recorded efficiently and quickly verified in a permanent way.

There are however a number of challenges which remain to be addressed. One such challenge is the reward each participant receives for finding a valid block. For bitcoin, a cryptocurrency which also works based on the proof-of-work concept, a network participant is rewarded in bitcoin for each block which they successfully solve in addition to the transaction fees for the transactions recorded in the block. Another challenge is the choice of proof-of-stake algorithm. Certain algorithms may benefit actors who are able to create specialised hardware optimised for computing the chosen algorthim, giving them an added advantage. Last but not least is the challenge of getting enough people incentivised to join the network (which ties into the rewards given).

Despite there being significant challenges which need to be addressed, the idea behind an open, distributed ledger has the potential to be a foundational technology for truly global space traffic management.

It would certainly be a welcome improvement over multiple space debris catalogues, each curated differently and containing different sorts of information.

This blogpost is based on the whitepaper: [SpOCChain Whitepaper: Validated & Trustworthy Distributed Space Object Catalog Generation Using Blockchains](https://www.stugrey.com/documents/SpOCChain_Whitepaper.pdf), by Dr. Stuart Grey
