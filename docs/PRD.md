# PRD --- Online Duel Table (Yu-Gi-Oh Social Tabletop)

**Version:** 1.0\
**Author:** Ewerton Azevedo\
**Date:** 2026\
**Status:** Draft

------------------------------------------------------------------------

# 1. Product Vision

Online Duel Table is a web platform that allows players to duel using a
**digital tabletop board synchronized in real time**, replicating the
experience of playing a physical card game.

Unlike traditional simulators, the platform **does not enforce game
rules automatically**. Players manually perform actions and apply rules
themselves, similar to playing in person.

The system focuses on:

-   Social gameplay
-   Card collection
-   Deck building
-   Real‑time duels
-   Card economy and betting

------------------------------------------------------------------------

# 2. Problem

TCG players often struggle to play remotely with friends because:

-   They do not always have their physical cards
-   Existing simulators are too rigid
-   Some platforms enforce complex rules automatically
-   Social interaction is limited

Online Duel Table solves this by providing a **simple digital tabletop
where players control everything manually**.

------------------------------------------------------------------------

# 3. Product Goals

### Primary Goal

Enable players to duel online with friends in a digital tabletop
environment.

### Secondary Goals

-   Provide a card collection system
-   Allow deck building
-   Implement a virtual card economy
-   Encourage social interaction between players
-   Introduce risk/reward mechanics through card betting

------------------------------------------------------------------------

# 4. Target Audience

Primary users:

-   Yu‑Gi‑Oh players
-   Trading card game players
-   Friends who want to duel online casually

Secondary users:

-   Collectors
-   Competitive duelists interested in betting cards

------------------------------------------------------------------------

# 5. Core Features

## 5.1 Multiplayer Duel Board

A real‑time shared board where two players interact.

Players can perform the following actions:

-   Draw card
-   Place card on field
-   Flip card
-   Change attack/defense position
-   Send card to graveyard
-   Banish card
-   Adjust Life Points
-   Move cards between zones

Game rules are **not enforced by the system**.

Players are responsible for following rules.

------------------------------------------------------------------------

# 6. Deck Builder

Players can create and manage decks using cards they own.

Features:

-   Create decks
-   Add/remove cards
-   Search cards
-   Filter by:
    -   Name
    -   ATK
    -   DEF
    -   Type
    -   Attribute
    -   Level

No deck construction rules are enforced initially.

------------------------------------------------------------------------

# 7. Card Collection System

Players maintain a personal inventory of cards.

Data model concept:

Cards Database - card_id - name - atk - def - level - type - attribute -
image

Player Inventory - player_id - card_instance_id - card_id

Each card instance is unique to allow betting and trading.

------------------------------------------------------------------------

# 8. Card Album (Binder)

Players can view their full collection.

Features:

-   Browse owned cards
-   View card statistics
-   See how many players own a specific card

Example statistics:

-   Total copies in the game
-   Number of players who own the card

------------------------------------------------------------------------

# 9. Starter Decks

New players choose one of three starter decks when joining the game.

Example concept:

-   Deck A
-   Deck B
-   Deck C

Each deck contains a predefined set of cards.

------------------------------------------------------------------------

# 10. Card Acquisition

Players obtain new cards through several methods.

## 10.1 Booster Packs

Players can buy booster packs using in‑game currency.

Each booster contains a random set of cards.

Example:

5 cards per pack.

Rarity probabilities:

-   Common
-   Rare
-   Super Rare
-   Ultra Rare

------------------------------------------------------------------------

## 10.2 Rotating Card Shop

Players can buy individual cards from a shop.

Rules:

-   Only \~10 cards available at a time
-   Shop refreshes every hour

Purpose:

-   Encourage market dynamics
-   Prevent direct access to every card

------------------------------------------------------------------------

# 11. Duel Betting System

Before a duel starts, players can bet a card.

Flow:

1.  Player A selects a card to bet
2.  Player B selects a card to bet
3.  Cards are removed from inventories
4.  Cards remain locked during the duel
5.  Winner receives both cards

Winner is determined by:

Player with remaining Life Points at duel end.

------------------------------------------------------------------------

# 12. In‑Game Currency

Players use currency to buy boosters and shop cards.

Ways to earn currency:

-   Starting bonus
-   Daily login rewards
-   Duel participation rewards

Optional future additions:

-   Selling duplicate cards
-   Tournament rewards

------------------------------------------------------------------------

# 13. Player Discovery System

Players can search for other players.

Filters may include:

-   Possession of a specific card
-   Player reputation
-   Online status

Players can:

-   Send duel invitations
-   Start chats
-   Negotiate bets

------------------------------------------------------------------------

# 14. Open Bet Market

Players can create public duel bets.

Example:

Player posts:

"Betting Dark Magician"

Other players can challenge the bet.

------------------------------------------------------------------------

# 15. Chat System

Players can communicate through chat.

Uses:

-   Negotiating bets
-   Discussing duels
-   Social interaction

Future upgrades may include:

-   Voice chat
-   Video chat

------------------------------------------------------------------------

# 16. Player Profile

Each player has a public profile.

Information displayed:

-   Duel history
-   Reputation score
-   Rare cards owned
-   Total duels played

------------------------------------------------------------------------

# 17. Reputation and Reporting

Since rules are not automated, a reporting system is required.

Players can report others for:

-   Cheating
-   Refusing bets
-   Toxic behavior

Reports affect a player's reputation score.

Low reputation players may have restricted access to betting features.

------------------------------------------------------------------------

# 18. Duel History

Each duel is recorded.

Stored data:

-   Players
-   Bet cards
-   Winner
-   Timestamp

Purpose:

-   Dispute resolution
-   Statistics
-   Player profiles

------------------------------------------------------------------------

# 19. Future Features

Possible future expansions:

-   Voice chat during duels
-   Video camera support
-   Ranked duel system
-   Card trading marketplace
-   Tournaments
-   Mobile support

------------------------------------------------------------------------

# 20. Technical Overview

Frontend:

-   Next.js
-   React
-   WebSocket
-   WebRTC (future voice/video)

Backend:

-   Python
-   FastAPI
-   WebSocket server

Database:

-   PostgreSQL

Realtime features:

-   Socket-based room system
-   Shared game state synchronization

------------------------------------------------------------------------

# 21. MVP Scope

The first release should include:

-   Account system
-   Multiplayer duel board
-   Card inventory
-   Deck builder
-   Starter decks
-   Booster packs
-   Card betting
-   Basic chat

Features postponed for later:

-   Voice/video chat
-   Reputation system
-   Open bet market
-   Player discovery filters

------------------------------------------------------------------------

# 22. Success Metrics

Metrics used to evaluate product success:

-   Number of duels played
-   Active daily players
-   Booster packs opened
-   Cards bet between players
-   Player retention

------------------------------------------------------------------------

# 23. Risks

Potential risks include:

-   Players abusing manual rule system
-   Toxic behavior between players
-   Economic imbalance in card distribution

Mitigation strategies:

-   Reputation system
-   Reporting tools
-   Moderation tools

------------------------------------------------------------------------

# 24. Conclusion

Online Duel Table focuses on providing a **social, flexible and
collectible card game experience**.

By avoiding complex rule engines and emphasizing player interaction, the
platform enables a lightweight yet engaging environment for online
dueling.
