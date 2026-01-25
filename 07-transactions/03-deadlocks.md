# Deadlocks

## Overview

A deadlock occurs when two or more transactions block each other by holding locks on resources the others need.

## Example

Transaction 1 locks row A and needs row B.
Transaction 2 locks row B and needs row A.

Neither can proceed, resulting in a deadlock.

## Handling Deadlocks

- Most databases detect deadlocks and abort one transaction.
- Design transactions to access resources in the same order.

## Practice

Explain how deadlocks can be prevented in SQL transactions.
