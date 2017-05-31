# Chatterbox

Chatterbox is a system for managing organizational ChatOps.

## Architecture

* API Server - Provides an API front end for receiving object-state-transition messages.
* Audit Service - Stores information about messages received and sent, provides reports of same.
* Pub/Sub Service - Provides channel mechanisms and rules engine for routing.
* Distribution Service - Routes messages to subscribers and manages rules for same.
* Admin Site - a website that provides information about the services above.

## Workflows

An administrator defines a message source, zero or more translations, one or more channels, one or more recipient groups, and one or more transmission adapters. Messages are sent from the source, identified by the API server, translated, and directed to channels.

On the distribution service, channel listeners wait for messages on known channels and use transmission adapters to transmit those messages to recipients.

## Data structures

* User
* Message Source
* Translation
* Channel
* Recipient Group
* Recipient
* Transmission Adapter
