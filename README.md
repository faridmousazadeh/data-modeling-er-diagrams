# Data Modeling: ER and Relational Diagrams

A portfolio of conceptual entity-relationship diagrams and logical relational models created for IST 659 Problem Set 6. The diagrams show how business requirements can be expressed with entities, attributes, cardinality, associative tables, keys, and foreign-key relationships.

## Models

| File | Model | Focus |
| --- | --- | --- |
| `diagrams/sales-quotation.drawio` | Conceptual ERD | Customer, quotation, and salesperson requirements; composite, derived, required, unique, and multivalued attributes |
| `diagrams/customer-addresses.drawio` | Logical relational model | Customers and addresses linked through an associative relation |
| `diagrams/foo-bar-baz.drawio` | Conceptual ERD | Required/optional participation, one-to-many and many-to-many relationships, composite/multivalued attributes, and relationship attributes |
| `diagrams/Spotify.drawio` | Conceptual ERD | Users, songs, playlists, and listening history |
| `diagrams/rideshare.drawio` | Logical relational model | Drivers, passengers, vehicles, locations, and rideshares |
| `diagrams/quotation.drawio` | Logical relational model | Quotations linked to customers and salespeople, with certification associations |

## Spotify requirements

The Spotify model is based on the requirements and design assumptions documented in [`docs/spotify-requirements.md`](docs/spotify-requirements.md). The original ERD is conceptual; it does not claim to be a deployed schema or include implementation-specific SQL.

## Opening the diagrams

Open any `.drawio` file in [diagrams.net](https://app.diagrams.net/) or the Draw.io desktop application. The native editable files are included.

## Scope and provenance

These diagrams are based on the author's IST 659 Problem Set 6 coursework. The public portfolio contains diagram source and explanatory notes only; it omits the submitted Word form, screenshots, student email, and personal reflection. The additional Spotify requirements note makes the modeling assumptions explicit for readers.
