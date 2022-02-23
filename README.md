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
- Manager application - works as an experience gateway
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

The next set of objects is related to the events. Every user can.

- Create an event (this is an abstract event, might mean reoccuring)
- Create a tickets for that (each ticket has additional properties, including the maximum number of usages, and rank for receiving dividends)
- Tickets can be purchased by NEAR tokens
- Each ticket holds a number of usages.
- If NEAR tokens are sent to the event, then they are distributed as dividends to the token holders based on the rank (any remainder remains in the contract)
- Tickets can be sold to the other person.

Finally, the last piece are crafter items. These looks like a typical NFTs. These works like a classical NFT.
They are created by the satelite applications. And they consume the badges during the creation.

### Manager Application

This is the application that works as an entry point.
**The default style is that the end user doesn't know about blockchain at all.**

Main functions

- See the status - summary, badges, identity, measures
- Discover events - see what events are around
- Discover apps - discover sattelite apps (described in the next chapter)
- Event manager - create and manage your own events
- Ticket market place - buy and use tickets
- NFT marketplace - marketplace for virtual assets

### Sattelite Applications

These are the applications connected to the ecosystem.
Each app can do a different things. Here are some examples:

- Measure your body shape from photos and grant badges for that.
- Application that realizes in person meeting.
- Application measuring the step (i.e. walk) activity and granting badges for that.
- Application for coach that compares the moves of students with professionals to monitor the progress. If student improves,
- Application that tracks certain web for results of an events. If user appears in the results, then particular badges can be assigned.
- Consume badges to craft an NTF.
- Game that uses NFTs.
