# Data Modeling: ER and Relational Diagrams

## Overview

This repository contains data-modeling coursework from IST 659 Problem Set 6. It includes conceptual entity-relationship diagrams and logical relational models. The conceptual diagrams express entities, attributes, and relationships; the logical models represent relationships using tables and key concepts.

These are modeling artifacts. They do not represent databases deployed from this repository.

## Course

**IST 659 — Data Administration Concepts and Database Management**  
Syracuse University

## Objectives

The diagrams demonstrate how to represent requirements as entities, attributes, and relationships, and how to express relationship cardinality and participation. The logical relational models show table relationships, key concepts, and associative relationships where they appear in the diagrams.

## Technical Skills

- Entity-relationship modeling
- Logical relational data modeling
- Entities and attributes
- Relationship cardinality and participation
- Primary-key and foreign-key concepts in the logical models
- Associative or bridge relationships where represented
- Draw.io / diagrams.net

## Models

| Diagram | Model type | Modeling focus |
| --- | --- | --- |
| [`sales-quotation.drawio`](diagrams/sales-quotation.drawio) | Conceptual ER diagram | Customer, quotation, and salesperson requirements, including composite, derived, required, unique, and multivalued attributes |
| [`foo-bar-baz.drawio`](diagrams/foo-bar-baz.drawio) | Conceptual ER diagram | Required and optional participation; one-to-many and many-to-many relationships; composite and multivalued attributes; relationship attributes |
| [`Spotify.drawio`](diagrams/Spotify.drawio) | Conceptual ER diagram | Users, songs, playlists, and listening history |
| [`customer-addresses.drawio`](diagrams/customer-addresses.drawio) | Logical relational model | Customers and addresses connected through an associative relation |
| [`rideshare.drawio`](diagrams/rideshare.drawio) | Logical relational model | Drivers, passengers, vehicles, locations, and rideshares |
| [`quotation.drawio`](diagrams/quotation.drawio) | Logical relational model | Quotations related to customers and salespeople, including certification associations |

## Spotify Requirements

[`docs/spotify-requirements.md`](docs/spotify-requirements.md) documents the requirements and design assumptions associated with the Spotify conceptual ER diagram. It describes the entities, attributes, and relationship cardinalities represented by that model.

The Spotify diagram remains conceptual. The requirements document records the requirements and design assumptions associated with the Spotify conceptual ER diagram.

## Project Structure

```text
diagrams/   Editable conceptual ER diagrams and logical relational models
docs/       Modeling notes and Spotify requirements/design assumptions
README.md   Project overview and diagram guide
```

## Key Takeaways

This coursework demonstrates two related modeling stages: describing requirements through conceptual ER diagrams and representing selected designs as logical relational models. The diagrams show relationships, cardinality, participation, key concepts, and associative relationships where present.

## Course Context

These artifacts are from **IST 659 Problem Set 6** at Syracuse University. The repository presents the diagram source and explanatory notes as part of an academic portfolio.

## Scope and Limitations

This repository contains diagrams and documentation, not SQL scripts or a deployed database. The diagrams do not claim to provide database-specific data types, constraints, indexes, or implementation behavior. The Spotify requirements note records model assumptions; it does not turn the conceptual diagram into a completed logical schema.
