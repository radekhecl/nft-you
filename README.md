# NFT You

The most valuable NFT, is you. And you need to care about yourself.
Metaverse, virtual reality, games, all these are awesome without the doubt.
However there is a significant drawback. It's easier than ever to fall into it and loose the connection with reality (with all the consequences).
This is not good. Therefore the NFT you project aims to create a synergy in between the real world and metaverse.

The core concept idea is that user get rewards in the form of badges for actions taken in the real world.
Examples of such action might be weight loss, travelling to the specific place, attending an event, meeting with other person.
These rewards can then be used to craft the items for the virtual worlds. More rewards means better items.
For example to craft a sword, you will need to have at least one badge related to the physical ability.

**Monetization.** The whole project will have 2 forms of monetizations

- Selling tickets. Everyone can issue a ticket series. Which is technically just NFT coming with a contract behind it. This might mean ticket for a certain event, or a sponsorship ticket with follow up dividend rights.
- NFT market place. All itmes (crafter NFTs, and tickets) can be resold. Contract will take the comission out of each resale (probably fixed).

**Note:** There are also a gas fees, but I would like to find the way how to make them zero for people who are participating.

## Technical Concept

The whole ecosystem is composed from the 2 things.

- Smart Contract(s) - data warehouse
- Sattelite Applications - heart that moves the world

### Smart Contract

This is where the data lives. User can always recover the account with the private key.

The center of the application is YOU. Each YOU has the following properties.

- badges - collection of badges awarded
  -  key - badge main key
  -  subkey - badge sub key
  -  score - achieved score (0 if the score is not relevant)
  -  timestamp - when badge was awarded
  -  consumed - whether badge was consumed
- identity - some satelite applications might store identity data (e.g. face descriptor) to prove that the user later on is the same person as before
  - key - key that defines what identity it is (e.g. face-haar)
  - version - version of the data
  - timestamp - timestamp of taken the identity
  - data - data blob (probably JSON or base64 string)
- measures - 
  - key - key that defines what measurement it is (e.g. body-shape)
  - version - version of the data
  - timestamp - timestamp of the measurement
  - data - data blob (probably JSON or base64 string)

Now the next objects are related to tickets. Everyone can create an event, and issue a ticket series for that.

Finally, the last piece are crafter items. These looks like a typical NFTs.

### Sattelite Applications

These are a bunch of applications that create, and consume the badges.
