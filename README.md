# Exploring Cadence with Flow

## Notes

### Cadence Notes

- On Flow Cadence, smart contracts are upgradeable. If you make a mistake, you can often update it, constrained by some rules, in a public and transparent manner.

- Cadence is a resource-oriented programming language that introduces new features to smart contract programming

- Attachments are a feature of Cadence designed to allow developers to extend a struct or resource type (even one that they did not create) with new functionality, without requiring the original author of the type to plan or account for the intended behavior.

- The view annotation indicates that the function is permitted to view, but not modify blockchain state.

- Each user has an account controlled by one or more private keys with configurable weight. This means that support for accounts/wallets with multiple controllers is built into the protocol by default.

- The move operator `<-` is unique to Cadence and is used to move resource types from one location to another. It works similar to the assignment operator `=` you're used to from most programming languages, except that the data in the location on the right side of the statement is destroyed by the operation

- The force-assignment operator `<-!` assigns a resource-typed value to an optional-typed variable if the variable is nil. If the variable being assigned to is non-nil, the execution of the program aborts.
The force-assignment operator is only used for resource types.

- The binary swap operator `<->` can be used to exchange the values of two variables. It is only allowed in a statement and is not allowed in expressions

- `@` symbol to specify that a type is a resource

### Flow notes

- Flow was built by consumer-facing, onchain app developers to solve the problem of building consumer-facing, onchain apps

- It is based on a unique multi-role architecture, and designed to scale without sharding, allowing for massive improvements in speed and throughput while preserving a developer-friendly, ACID-compliant environment.

- It natively allows development of smart contracts in the powerful Cadence language, and also supports full Ethereum Virtual Machine (EVM) equivalence with contracts written in Solidity.

- Native VRF: Flow provides onchain randomness at the protocol level.

- flow-cli is used to dependency management

- Flow has native support for multi-sig transactions since all accounts are defined as smart contracts. Flow provides support for multiple keys to be added to an account and weights can be applied to denote relative priority.

- Flow has built-in support for 3 different roles for transactions which provides native support for sponsored transactions.

- Flow has a comprehensive list of sdks

## Bugs

- As of v2.2.19 : The installation script for flow-cli does not work. I had to get imaginative and install it with this command

```bash
go install github.com/onflow/flow-cli/cmd/flow@latest
```

which is not indicated as an installation option.

## Instructions

### With local installation

Requirements: Go >= 1.24.2 or flow-cli 

Flow cli : https://developers.flow.com/tools/flow-cli/install

or install hack

```bash
go install github.com/onflow/flow-cli/cmd/flow@latest
```


```bash
git clone https://github.com/Neal-C/exploring_cadence_flow.git
```

```bash
cd exploring_cadence_flow
```

```bash
flow test
```

## Resources 

- https://cadence-lang.org/
- https://developers.flow.com/
- https://developers.flow.com/tools/flow-cli/install