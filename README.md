# Islandora Object Field

## Warning: Experimental Module

This module is very much an experiment and probably not in a production-ready
state, bugs and errors are likely.

## Introduction

Provides a new field type, widget and formatter for "Islandora Object". On the
developer side integrates with the entity api to provide easier access to the
referenced object when developing.

## Requirements

- [Islandora](https://github.com/islandora/islandora)
- [Entity API](https://www.drupal.org/project/entity)

## Installation

Enable the module as usual.

## Configuration

Add a new field to any drupal entities with the field type "Islandora object" to
provide a direct reference to Islandora objects.  Can be optionally limited by 
object cmodel.

## Alternatives

This module **only** aims to provide a field for referencing Islandora objects,
there are a couple of other modules that provide some actual data syncing and 
views integration (and therefore integration with the entity reference module):

- [Islandora Entity Bridge](https://github.com/btmash/islandora_entity_bridge)
- [Islandora Sync](https://github.com/Islandora-Labs/islandora_sync)

## Maintainers/Sponsors

Current maintainer:

- [Luke Bainbridge](https://github.com/midnightluke)

## License

[GPLv3](http://www.gnu.org/licenses/gpl-3.0.txt)
