      * [namespace HearthMirror:](#namespace-hearthmirror)
         * [Reflection Class:](#reflection-class)
         * [Status class](#status-class)
      * [HearthMirror.Objects namespase](#hearthmirrorobjects-namespase)
         * [AccountId object](#accountid-object)
         * [ArenaInfo object](#arenainfo-object)
         * [BattleTag object](#battletag-object)
         * [BrawlInfo object](#brawlinfo-object)
         * [Card object](#card-object)
         * [Deck object](#deck-object)
         * [GameServerInfo object](#gameserverinfo-object)
         * [MatchInfo object](#matchinfo-object)
         * [MatchInfo.Player object](#matchinfoplayer-object)
         * [RewardData objects](#rewarddata-objects)
         * [SeasonEndInfo object](#seasonendinfo-object)
         * [SetFilterItem object](#setfilteritem-object)
     
## namespace HearthMirror:

The main HearthMirror namespace, containing the other Namespaces as well.

### Reflection Class:

The main class to obtain information from the game.

#### List\<Card\> `GetCollection()`:

Returns the player's collection. Card is of type `HearthMirror.Objects.Card`.

#### List\<Deck\> `GetDecks()`:

Returns decks in a pleyer's collection. Deck is of type `HearthMirror.Objects.Deck`.

#### GameServerInfo `GetServerInfo()`

#### Int `GetGameType()`:

(insert what different numbers mean here)

#### Bool `IsSpectating()`:

Whether or not someone is currently spectating someone.

#### Long `GetSelectedDeckInMenu()`:

Returns DeckID of a deck in the player's collection.

#### MatchInfo `GetMatchInfo()`

#### ArenaInfo `GetArenaDeck()`:

Gets the current arena deck.

#### List\<Card\> `GetArenaDraftChoices()`:

Returns a list of the 3 current arena drafting choices.

#### int `GetFormat()`:

returns the format the player currently has selected.

#### Deck `GetEditedDeck`:

Gets the edited deck.

#### Bool `IsFriendsListVisible()`

#### Bool `IsGameMenuVisible()`

#### bool `IsOptionsMenuVisible()`

#### bool `IsMulligan()`

#### int `GetNumMulliganCards()`

#### bool `IsChoosingCard()`

#### int `GetNumChoiceCards()`

#### bool `IsPlayerEmotesVisible()`

#### bool `IsEnemyEmotesVisible()`

#### bool `IsInBattlecryEffect()`

#### bool `IsDragging()`

#### bool `IsTargetingHeroPower()`

#### int `GetBattlecrySourceCardZonePosition()`

#### bool `IsHoldingCard()` 

#### bool `IsTargetReticleActive()`

#### bool `IsEnemyTargeting()`

#### bool `IsGameOver()`

#### bool `IsInMainMenu()`

#### UI_WINDOW `GetShownUiWindowId()`

#### bool `IsPlayerHandZoneUpdatingLayout()`

#### bool `IsPlayerPlayZoneUpdatingLayout()`

#### SceneMode `GetCurrentSceneMode()`

#### int `GetNumCardsPlayerHand()`

#### int `GetNumCardsPlayerBoard()`

#### int `GetNavigationHistorySize()`

#### int `GetCurrentManaFilter()`

#### SetFilterItem `GetCurrentSetFilter()`

#### BattleTag `GetBattleTag()`

#### List\<Card\> `GetPackCards()`

Returns a list of 5 cards from the latest pack.

#### List\<RewardData\> `GetArenaRewards()`

Returns the Arena rewards. It would be best to make sure the client is looking at their arena rewards before calling.

#### SeasonEndInfo `GetSeasonEndInfo()`

Gets the end-of-season rewards. It would be best to make sure the client is looking at their arena rewards before calling.

#### int `GetLastOpenedBoosterId()`

Returns the last (booster) card pack ID

#### AccountId `GetAccountId()`

Returns the Account ID of the Bnet player (more information needed).

#### BrawlInfo `GetBrawlInfo()`

Returns brawl info.

### `Status` class

Used to see the status of HearthMirror. 

#### MirrorStatus `MirrorStatus`

Gets the current MirrorStatus

#### Exception `Exception`

Gets the current Exception (if there is one)

#### Status `GetStatus()`

Returns `Mirrorstatus.Ok` if HearthMirror is ready, otherwise returns the `exception` itself.

Example usage: 

```C#
if (Status.GetStatus().MirrorStatus == MirrorStatus.Ok)
    {
        //do stuff with Reflection
    }
```

## `HearthMirror.Objects` namespase

types that HearthMirror uses

### `AccountId` object

#### ulong `Hi` (get; set;)

#### ulong `Lo` (get; set;)

### `ArenaInfo` object

#### Deck `Deck` (get; set;)

#### int `Losses` (get; set;)

#### int `Wins` (get; set;)

#### int `CurrentSlot` (get; set;)

#### List\<RewardData\> `Rewards` (get; set;)

### `BattleTag` object

#### string `Name` (get; set;)

#### int `Number` (get; set;)

### `BrawlInfo` object

#### int `MaxWins` (get; set;)

#### bool `IsSessionBased`

true if `MaxWins` or `MaxLosses` is more than 0

#### int `Wins` (get; set;)

#### int Losses (get; set;)

#### int GamesPlayed (get; set;)

#### int WInStreak (get; set;)

### `Card` object

#### string `Id` (get;)

#### int `Count` (get; set;)

#### bool `Premium` (get;)

true if the card is golden.

#### Constructor `Card(string id, int count, bool premium)`

### `Deck` object

#### long `Id` (get; set;)

#### string `Name` (get; set;)

#### string `Hero` (get; set;)

#### bool `IsWild` (get; set;)

#### int `Type` (get; set;)

#### int `SeasonId` (get; set;)

#### int `CardBackId` (get; set;)

#### int `HeroPremium` (get; set;)

Likely if the hero is not one of the default 9

#### List\<Card\> `Cards` (get; set;)

### `GameServerInfo` object

#### string `Address` (get; set;)

#### string `AuroraPassword` (get; set;)

???

#### long `ClientHandle` (get; set;)

#### int `GameHandle` (get; set;)

#### int `Mission` (get; set;)

#### int `Port` (get; set;)

#### bool `Resumable` (get; set;)

#### bool `SpectatorMode` (get; set;)

#### string `SpectatorPassword` (get; set;)

#### string `Version` (get; set;)

### `MatchInfo` object

#### Player `LocalPlayer` (get; set;)

#### Player `OpposingPlayer` (get; set;)

#### int `BrawlSeasonId` (get; set;)

#### int `MissionId` (get; set;)

#### int `RankedSeasonId` (get; set;)

### `MatchInfo.Player` object

#### string `Name` (get; set;)

#### int `Id` (get; set;)

#### int `StandardRank` (get; set;)

#### int `StandardLegendRank` (get; set;)

#### int `StandardStars` (get; set;)

#### int `WildRank` (get; set;)

#### int `WildLegendRank` (get; set;)

#### int `WildStars` (get; set;)

#### int `CardBackId` (get; set;)

#### constructor `Player(int id, string name, int standardRank, int standardLegendRank, int standardStars, int wildRank, int wildLegendRank, int wildStars, int cardBackId)`

### RewardData objects

#### ArcaneDustRewardData

int `Amount` (get;)

constructor `ArcaneDustRewardData(int amount)`

#### BoosterPackRewardData

int `Id` (get;)

int `count` (get;)

constructor `BoosterPackRewardData(int id, int count)`

#### CardRewardData

string `Id` (get;)

int `Count` (get;)

bool `Premium` (get;)

constructor `CardRewardData(string id, int count, bool premium)`

#### CardBackRewardData

int `Id` (get;)

constructor `CardBackRewardData(int id)`

#### ForgeTicketRewardData

int `Quantity` (get;)

constructor `ForgeTicketRewardData(int quantity)`

#### GoldRewardData

int `Amount` (get;)

constructor `GoldRewardData(int amount)`

#### MountRewardData

int `MountType` (get;)

constructor `MountRewardData(int mountType)`

### `SeasonEndInfo` object

#### int `BonusStars` (get;)

#### int `BoostedRank` (get;)

#### int `ChestRank` (get;)

#### bool `IsWild` (get;)

#### int `LegendRank` (get;)

#### int `Rank` (get;)

#### int `SeasonId` (get;)

#### list\<RewardData\> `RankedRewards` (get;)

#### constructor `SeasonEndInfo(int bonusStars, int boostedRank, int chestRank, bool isWild, int legendRank, int rank, int seasonId, List<RewardData> rankedRewards)`

### `SetFilterItem` object

#### bool `IsAllStandard` (get; set;)

#### bool `IsWild` (get; set;)
