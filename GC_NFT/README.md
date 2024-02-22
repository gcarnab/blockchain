# GCARNAB NFT REPOSITORY
___

By GCARNAB <a href='https://github.com/gcarnab'> <img src='https://avatars.githubusercontent.com/u/15156604?v=4' width="50"/></a>
___

## Contents

- 

## Resources

- **Video Tutorial 2023 ITA :** https://youtu.be/eU3fetZsx9E?si=EutC4tvQ-8JGgmYx
- **Video Tutorial 2024 EN :** https://youtu.be/ShlX50vs-iM?si=nVhy2DZACeFb4-2y
- **Guida IT :** https://dayone.change-media.it/come-creare-un-nft/
- **Guida IT :** https://thecryptogateway.it/creare-nft/

## Tutorial

### Creare un NFT su OpenSea: Tutorial Completo

**Introduzione**:

Un NFT (Non-Fungible Token) è un asset digitale unico e non replicabile, la cui proprietà è registrata sulla blockchain. Gli NFT possono rappresentare opere d'arte, musica, video, oggetti da collezione e molto altro.In questo tutorial, ti mostreremo come creare un NFT su OpenSea, il marketplace più popolare per NFT.

1. **Scelta della Blochchain**
Per creare un NFT, spesso si sceglie una blockchain che supporta gli standard NFT come ERC-721 (Ethereum), ma ci sono anche altre opzioni come Binance Smart Chain (BEP-721) o Flow Blockchain.

2. **Preparazione dell'Ambiente**
- Installa un portafoglio crypto che supporti la blockchain scelta (es. MetaMask per Ethereum).
- Acquisisci criptovaluta per coprire le spese di transazione.

3. **Crea il Tuo Token**
Ethereum e ERC-721 (Esempio usando Solidity):
- Utilizza un ambiente di sviluppo come Remix o Truffle.
- Scrivi uno smart contract che segua lo standard ERC-721.
- Compila e distribuisci lo smart contract sulla blockchain.

```console
// Esempio di contratto ERC-721
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC721/ERC721.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract MyNFT is ERC721, Ownable {
    constructor() ERC721("MyNFT", "MNFT") {}

    function mint(address to, uint256 tokenId) public onlyOwner {
        _safeMint(to, tokenId);
    }
}
```

4. **Carica il Tuo NFT su OpenSea**:
- Accedi a OpenSea. https://opensea.io/ 
- Connetti il tuo portafoglio crypto (es. MetaMask). **NB: ogni profilo corrisponde ad un Address del wallet differente** 
- Nella parte superiore, fai clic su "Create".
- Fai clic su "Mint NFT" e compila i dettagli richiesti.
- Dopo aver creato la collezione, fai clic su "Add New Item".
- Inserisci le informazioni sul tuo NFT, tra cui il link all'immagine, il contratto e l'ID del token.
- Pubblica il tuo NFT.

5. **Minting (Creazione del Token)**
- Torna al tuo smart contract e chiama la funzione mint per creare nuovi token.
- Tramite OpenSea, gli acquirenti potranno visualizzare e acquistare i tuoi NFT.