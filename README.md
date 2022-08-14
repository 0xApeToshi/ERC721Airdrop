# ERC721Airdrop
## THIS CONTRACT WAS NOT FULLY TESTED OR AUDITED. USE FOR RESEARCH PURPOSES ONLY!

Create NFT airdrops for the cost deploying of a typical `ERC721` contract, no minting required!


# Example

````solidity
// SPDX-License-Identifier: MIT

pragma solidity ^0.8.4;

import "https://github.com/0xApeToshi/ERC721Airdrop/blob/main/ERC721Airdrop.sol";

/**
 * @title AirdropNFT
 * @dev Airdrop an NFT to all BAYC holders
 */
contract AirdropNFT is ERC721Airdrop {
    constructor()
        ERC721Airdrop(
            "AirdropNFT",
            "ANFT",
            0xBC4CA0EdA7647A8aB7C2061c2E118A18a936f13D, // source contract address
            0, // from `tokenId`
            9999 // to `tokenId`
        )
    {}
}
