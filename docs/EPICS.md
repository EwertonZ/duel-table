# Backlog --- Product Epics

Project: Online Duel Table

This document lists the main **Epics** for the project backlog. Each
Epic represents a major functional area of the system and will later be
broken down into **User Stories and Tasks**.

------------------------------------------------------------------------

# EPIC 01 --- Multiplayer Duel Board

Core feature of the platform: a shared real‑time duel table.

Main goals:

-   Two players connected in the same room
-   Real-time synchronization via WebSocket
-   Shared board state

Key capabilities:

-   Draw card
-   Move card between zones
-   Flip card
-   Change ATK / DEF position
-   Send card to graveyard
-   Banish card
-   Adjust Life Points

This Epic represents the **core gameplay experience**.

------------------------------------------------------------------------

# EPIC 02 --- Card Database Integration

Integration with external card data source.

Responsibilities:

-   Import card data
-   Store metadata locally
-   Load images and attributes

Possible source:

-   YGOPRODeck API

Card information includes:

-   Name
-   ATK
-   DEF
-   Level
-   Attribute
-   Type
-   Card image

------------------------------------------------------------------------

# EPIC 03 --- Player Card Inventory

System that manages the cards owned by each player.

Features:

-   Player inventory
-   Card instances
-   Card quantity tracking
-   Ownership validation

Important requirement:

Each card should exist as a **unique instance** so it can be:

-   bet in duels
-   transferred between players

------------------------------------------------------------------------

# EPIC 04 --- Deck Builder

Players can build and manage decks.

Core features:

-   Create deck
-   Edit deck
-   Delete deck
-   Add cards
-   Remove cards

Search features:

-   Search by name
-   Filter by ATK
-   Filter by DEF
-   Filter by type
-   Filter by attribute

Deck rules are **not enforced initially**.

------------------------------------------------------------------------

# EPIC 05 --- Booster Pack System

Players can acquire cards through boosters.

Features:

-   Purchase booster packs
-   Random card generation
-   Rarity probability system

Example rarities:

-   Common
-   Rare
-   Super Rare
-   Ultra Rare

Opening a booster adds cards to the player's inventory.

------------------------------------------------------------------------

# EPIC 06 --- Rotating Card Shop

A shop where players can buy individual cards.

Features:

-   Limited number of cards available
-   Periodic rotation (e.g., every hour)
-   Prices defined per card

Purpose:

-   Encourage scarcity
-   Prevent unlimited card access

------------------------------------------------------------------------

# EPIC 07 --- Duel Betting System

Players can bet cards before a duel.

Flow:

1.  Player A selects a card to bet
2.  Player B selects a card to bet
3.  Cards are locked during the duel
4.  Winner receives both cards

Winner is determined by:

Remaining Life Points at duel end.

------------------------------------------------------------------------

# EPIC 08 --- Player Profiles

Each player has a profile page.

Profile may include:

-   Duel history
-   Rare cards owned
-   Reputation score
-   Total duels played
-   Cards won through bets

Profiles support social interaction and credibility.

------------------------------------------------------------------------

# EPIC 09 --- Player Discovery System

Players can search for other players.

Filters may include:

-   Players who own a specific card
-   Online players
-   Reputation level

Players can:

-   View profiles
-   Send duel invitations
-   Start chat conversations

------------------------------------------------------------------------

# EPIC 10 --- Open Bet Market

Players can publicly post bets.

Example:

Player posts:

"Betting Dark Magician"

Other players can challenge that bet.

This creates a **marketplace of duels**.

------------------------------------------------------------------------

# EPIC 11 --- Chat System

Communication system between players.

Features:

-   Private chat between players
-   Chat in duel rooms
-   Negotiation of bets

Future extensions:

-   Voice chat
-   Video chat

------------------------------------------------------------------------

# EPIC 12 --- Reputation & Reporting System

Because duels are manually enforced, players must be able to report
misconduct.

Possible report reasons:

-   Cheating
-   Refusing agreed bet
-   Toxic behavior

System components:

-   Report submission
-   Moderation review
-   Reputation score impact

------------------------------------------------------------------------

# EPIC 13 --- Duel History

System to track past duels.

Stored information:

-   Players involved
-   Bet cards
-   Winner
-   Timestamp

Uses:

-   Profile statistics
-   Dispute resolution
-   Analytics

------------------------------------------------------------------------

# EPIC 14 --- Game Economy

Virtual currency used to acquire cards.

Ways to obtain currency:

-   Starting balance
-   Daily login rewards
-   Duel participation rewards

Currency is used for:

-   Booster packs
-   Shop cards

------------------------------------------------------------------------

# EPIC 15 --- Card Album (Binder)

A visual collection system for players.

Features:

-   View all owned cards
-   Browse full card database
-   See collection progress

Statistics available:

-   Total copies in the game
-   Number of players who own a card

This feature encourages collecting behavior.

------------------------------------------------------------------------

# Notes

This document defines only the **high-level Epics**.

Next step:

Break each Epic into:

-   User Stories
-   Acceptance Criteria
-   Development Tasks
