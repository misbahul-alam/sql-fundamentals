# ACID

## Overview

ACID stands for Atomicity, Consistency, Isolation, and Durability. These are the key properties that ensure reliable database transactions.

## Properties

- **Atomicity**: All operations in a transaction are completed; if not, the transaction is aborted.
- **Consistency**: A transaction brings the database from one valid state to another.
- **Isolation**: Transactions do not interfere with each other.
- **Durability**: Once a transaction is committed, it remains so, even in the event of a crash.

## Example

Transferring money between accounts should be atomic: both the debit and credit must succeed or fail together.

## Practice

Explain what would happen if a transaction was not durable.
