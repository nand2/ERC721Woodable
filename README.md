# ERC721Woodable

The goal of the ERC721Woodable extension is to add the ability to woodify your NFTs. Thus, you are able to mint **WNFTs** (wood NFTs) based on your NFTs.

## Advantages

* Natively as good as IPFS : it lives forever. You don't even need a pin server.
* Inherent heavy security: Your bored apes can be stolen with a scam transaction, your WNFTs cannot.
* You don't need to order a print, you can hang it directly to your wall.
* If the contract implements the extra ERC721WoodBurnable interface, more enjoyment can be extracted from watching your token burn. Plz follow safety procedures.
* Gas savings! Gas fees to send a WNFT are usually lower than Ethereum, plz make enquiry at your post office.
* Naturaly eco-friendly: Your NFT is made of bad PoW bits, or less-bad PoS bits; your WNFT is made of recyclable wood.

## Usage

Once installed, you can use the woodable extension this way : 

```solidity
pragma solidity ^0.8.9;

import "ERC721Woodable.sol";

contract Hexmap is ERC721, ERC721Woodable {

  function woodMint(uint256 tokenId) external payable {
      require(msg.value == woodificationPrice, "Incorrect price");
      require(ownerOf(tokenId) == msg.sender, "You must own the NFT");
      require(woodificationActive, "Woodification not active yet");

      _safeWoodMint(tokenId);
  } 
}
```

## Roadmap

* Create the ERC721WoodBurnable extension
* Add support for various minting experiences (lasercutting, CNC milling, ...)
* Optimizing the transfert speed of WNFTs


## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.
