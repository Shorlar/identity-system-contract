# DID Registration and Verification Contract

This contract allows users to register and verify Decentralized Identifiers (DID) using a zero-knowledge proof (zk-proof). It defines the necessary functions for registering a DID, retrieving a registered DID, and verifying the DID through zk-proof.

## Overview

- **DID**: A Decentralized Identifier (DID) is a globally unique identifier, represented here as a string (max 50 characters).
- **zk-proof**: A Zero-Knowledge Proof (zk-proof) is used to prove the validity of the DID, without revealing the actual information associated with it. The zk-proof is represented as a string (max 100 characters).

## Components

### `identities` Map
A map that holds the DID and zk-proof for each registered account. The key is the principal (account address), and the value is a tuple containing:
- `did`: A string representing the Decentralized Identifier (max 50 characters).
- `zk-proof`: A string representing the Zero-Knowledge Proof (max 100 characters).

```lisp
(define-map identities principal (tuple (did (string-ascii 50)) (zk-proof (string-ascii 100))))
