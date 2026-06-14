# LootLocker GraphQL Schema

This document describes the conceptual GraphQL schema derived from the LootLocker Game API, Server API, and Admin API REST surfaces. LootLocker is a game backend-as-a-service platform offering player authentication, leaderboards, virtual economies, inventories, persistent storage, progressions, and more.

Reference: https://ref.lootlocker.com/game-api/

---

## Overview

The schema maps LootLocker's REST API concepts into a typed GraphQL surface. All major resource domains are represented as named types, with query and mutation roots that mirror the operations available via the REST API.

---

## Type Inventory

### Player Domain

| Type | Description |
|---|---|
| `Player` | Top-level player record aggregating identity, session, inventory, and more |
| `PlayerInfo` | Basic public-facing player information |
| `PlayerDetails` | Extended player attributes including metadata and linked identifiers |
| `PlayerIdentifier` | A single platform identity linked to a player account (Steam, Epic, etc.) |

### Session Domain

| Type | Description |
|---|---|
| `Session` | An authenticated game session for a player |
| `SessionDetails` | Payload returned when a new session is created |
| `SessionToken` | The token used to authenticate subsequent game-client requests |
| `GameVersion` | Version and build metadata for the running game |

### Character Domain

| Type | Description |
|---|---|
| `Character` | A player-owned character slot |
| `CharacterDetails` | Extended attributes for a character |
| `CharacterType` | Template defining the shape of a character |

### Inventory & Asset Domain

| Type | Description |
|---|---|
| `Inventory` | A player or character inventory container |
| `InventoryDetails` | A single inventory entry — one instance of an asset |
| `Asset` | Full asset record from the asset catalogue |
| `AssetDetails` | Resolved asset data including context and metadata |
| `AssetType` | Classifies what kind of thing the asset is |
| `AssetClass` | Organises assets into logical class groupings |
| `AssetFiles` | Binary and structured data files attached to an asset |
| `AssetStorage` | Key-value storage embedded directly on an asset |

### Instance Domain

| Type | Description |
|---|---|
| `Instance` | A runtime reference to an asset instance in a player's inventory |
| `InstanceDetails` | Extended runtime details including per-instance key-value storage |

### Purchasing & Catalog Domain

| Type | Description |
|---|---|
| `Purchase` | A purchase transaction record |
| `PurchaseDetails` | Line-item detail within a purchase |
| `PurchaseStatus` | Current lifecycle state of a purchase |
| `DLC` | A downloadable content bundle |
| `DLCDetails` | Metadata and asset payload of a DLC bundle |
| `Catalog` | A virtual store catalog |
| `CatalogDetails` | Extended attributes of a catalog |
| `Listing` | A single item listing within a catalog |
| `ListingDetails` | Extended metadata for a catalog listing |
| `Price` | A price in a specific virtual or real currency |
| `CurrencyDetails` | A virtual or real currency definition |

### Progression Domain

| Type | Description |
|---|---|
| `ProgressionKey` | A key identifying a progression track |
| `Progression` | A player's current position on a progression track |
| `ProgressionDetails` | Full details of a progression record including tier history |
| `Steps` | The individual steps making up a progression tier boundary |
| `ProgressionTier` | A single tier within a progression track |
| `TierDetails` | Extended metadata for a progression tier |
| `TierReward` | A reward granted when a player reaches a tier |

### Leaderboard Domain

| Type | Description |
|---|---|
| `Leaderboard` | A leaderboard definition |
| `LeaderboardDetails` | Full configuration and rank list for a leaderboard |
| `Score` | A single score entry on a leaderboard |
| `Rank` | Ranking position data for a leaderboard entry |
| `Member` | Player or character representation on a leaderboard |
| `Submission` | A score submission request payload |

### Trigger & Drip Reward Domain

| Type | Description |
|---|---|
| `Trigger` | An event trigger that fires reward pipelines |
| `TriggerDetails` | Configuration for a trigger definition |
| `DripReward` | A reward dripped to a player when a trigger fires |

### Storage Domain

| Type | Description |
|---|---|
| `Storage` | Player or game persistent cloud storage |
| `StorageObject` | A single named storage object |
| `KeyValue` | A generic key-value pair used throughout the schema |

### Notification Domain

| Type | Description |
|---|---|
| `Notification` | A notification delivered to a player |
| `NotificationDetails` | Body and payload of a notification |
| `Priority` | Severity / importance level for a notification |

### Group Domain

| Type | Description |
|---|---|
| `Group` | A player group (guild, team, clan, etc.) |
| `GroupDetails` | Extended attributes of a group |
| `GroupMember` | A member entry within a group |

### File Domain

| Type | Description |
|---|---|
| `File` | A player-uploaded file stored on the LootLocker CDN |

### Challenge Domain

| Type | Description |
|---|---|
| `Challenge` | A challenge or mission definition |
| `ChallengeDetails` | Full configuration for a challenge or mission |

### Shared Utilities

| Type | Description |
|---|---|
| `Metadata` | Arbitrary metadata tag attached to various entities |

### Auth & Admin Domain

| Type | Description |
|---|---|
| `APIKey` | A game or server API key credential |
| `Token` | A short-lived JWT or opaque token for server-to-server calls |
| `Admin` | An admin user account on the LootLocker dashboard |
| `SDK` | SDK descriptor returned from the SDKs endpoint |

---

## Enums

| Enum | Values |
|---|---|
| `AuthProvider` | STEAM, EPIC_GAMES, PLAYSTATION, XBOX, NINTENDO_SWITCH, APPLE, GOOGLE, WHITE_LABEL, GUEST |
| `PurchaseStatusValue` | OPEN, FAILED, COMPLETED, CANCELLED |
| `NotificationPriority` | LOW, MEDIUM, HIGH, CRITICAL |
| `AssetVariantType` | DEFAULT, RENTAL, CONTEXT |

---

## Schema File

The full GraphQL SDL is at `lootlocker-schema.graphql` in this directory.

---

## Sources

- Game API Reference: https://ref.lootlocker.com/game-api/
- Server API Reference: https://ref.lootlocker.com/server-api/
- Admin API Reference: https://ref.lootlocker.com/admin-api/
- Documentation: https://docs.lootlocker.com/
