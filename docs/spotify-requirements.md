# Spotify conceptual ER requirements

## Scope

The source scenario describes a music streaming service that stores songs and genres, lets users create playlists, and records listening activity for analytics and artist credit. This document records the entity, attribute, and cardinality interpretation represented by the Spotify conceptual ERD.

## Entities and attributes

| Entity | Attributes from the scenario | Modeling notes |
| --- | --- | --- |
| User | name (required), email (required and unique), preferred genres (multivalued) | A user identifier is assumed for identity and relationship references; the scenario does not name its format. |
| Song | title (required), artist (required), genres (multivalued), length | A song identifier is assumed. The scenario does not state whether title is globally unique, so title is not treated as a key. |
| Playlist | created date (required) | A playlist identifier is assumed. Each playlist belongs to its creating user. |
| History | listen date/time (required) | A history identifier is assumed because a user may listen to the same song repeatedly. A timestamp is needed to distinguish events and support analytics. |

The original diagram treats genre and preferred genres as multivalued conceptual attributes. In a relational implementation, these would normally become genre lookup and bridge relations. A logical Spotify schema was not included in this assignment, so those implementation tables are not presented as completed coursework.

## Relationships and cardinalities

| Relationship | First direction | Reverse direction | Rationale |
| --- | --- | --- | --- |
| User creates Playlist | A user may create zero or many playlists. | Each playlist is created by exactly one user. | The scenario says users can build playlists and tracks the playlist creation date. |
| Playlist contains Song | A playlist contains one or more songs. | A song may appear on zero or many playlists. | One playlist can contain multiple songs; songs may be reused. |
| User has listening History | A user may have zero or many history records. | Each history record belongs to exactly one user. | Each archived listening event is attributable to a listener. |
| History records Song | Each history record records exactly one song. | A song may appear in zero or many history records. | Repeated listens are separate history events. |

## Assumptions and boundaries

- User, song, playlist, and history identifiers are implicit modeling keys; their physical data types and generation rules are unspecified by the scenario.
- “Artist” is represented as a required song attribute to match the assignment wording. A fuller catalog design could model artists as a separate entity and support multiple credited artists per song.
- The listening timestamp is represented as a required event attribute. The assignment says to archive any song listened to, which implies a listening event record; it does not define playback completion or partial-listen rules.
- This is a conceptual design exercise. No database, sample dataset, security policy, or production behavior is asserted.
