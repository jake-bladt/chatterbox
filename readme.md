# Chatterbox

Chatterbox is a system for managing organizational ChatOps.

## Architecture

* API Server - Provides an API front end for receiving object-state-transition messages.
* Audit Service - Stores information about messages received and sent, provides reports of same.
* Pub/Sub Service - Provides channel mechanisms and rules engine for routing.
* Distribution Service - Routes messages to subscribers and manages rules for same.

## data structures


