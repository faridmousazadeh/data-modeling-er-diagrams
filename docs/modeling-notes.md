# Modeling notes

## Conceptual versus logical models

The conceptual diagrams communicate entities, attributes, relationship names, and participation/cardinality without binding the design to a particular DBMS. The logical diagrams translate relationships into tables, primary keys, foreign keys, and associative tables.

## Relational mapping examples

- `customer-addresses.drawio` models a many-to-many customer/address association with `customer_addresses`; the composite key prevents duplicate pairings.
- `rideshare.drawio` places vehicle, driver, passenger, pickup, and drop-off foreign keys on the rideshare relation. Pickup and drop-off reference the same location entity in distinct roles.
- `quotation.drawio` separates salesperson certifications into a bridge relation and stores quotation references to the customer and salesperson.

## Interpretation cautions

- The diagrams capture the assignment-level designs; they do not include database-specific data types, check constraints, indexes, authorization, or migration scripts.
- In `foo-bar-baz.drawio`, guzzle attributes belong to the Bar–Baz relationship and therefore require an associative entity when mapped to a relational schema.
- The Spotify diagram remains conceptual. See the assumptions in `spotify-requirements.md` before treating it as a logical database design.
