### **NOTE: Not ready for public use. Please send a [twitter](https://twitter.com/0xOlias) dm if you're interested in using Ponder.**

# Ponder

A framework for blockchain-enabled web services

## Features

|                          | ponder                       | Graph Protocol                                 |
| ------------------------ | ---------------------------- | ---------------------------------------------- |
| Local dev server         | ✅                           | ❌                                             |
| Hot reloading            | ✅                           | ❌                                             |
| Debug with `console.log` | ✅                           | ❌                                             |
| Import NPM packages      | ✅                           | ❌                                             |
| Hosting requirements     | Node.js; Postgres (optional) | Graph Node; IPFS node; Ethereum node; Postgres |
| Supported networks       | Any EVM blockchain           | Ethereum mainnet only[^1]                      |

## Quickstart

### I'm replacing a Graph Protocol subgraph

Ponder is an alternative to the Graph Protocol. You can quickly migrate an existing subgraph repository to Ponder using the `create-ponder` CLI tool.

#### 1. Run `create-ponder`

This command will create a project folder called `ponder` in the current working directory. Include the `--from-subgraph` option to bootstrap your project using an existing Graph Protocol subgraph.

```
npm init ponder -- --from-subgraph [path]
# or
pnpm create ponder --from-subgraph [path]
# or
yarn create ponder --from-subgraph [path]
```

#### 2. Start the development server

```shell
cd ponder
```

```shell
npm run dev
# or
yarn dev
# or
pnpm run dev
```

The dev server prints logs to help you debug any configuration issues or errors. The server automatically reloads whenever you save changes in any project file.

#### 3. Write event handlers

Ponder event handler functions are similar to Graph Protocol mapping functions. [More docs here](https://github.com/0xOlias/ponder/blob/main/docs/writing-event-handlers.md).

## Guides

[Configuring contracts & networks](https://github.com/0xOlias/ponder/blob/main/docs/event-sources-and-networks.md)

[Writing event handlers](https://github.com/0xOlias/ponder/blob/main/docs/writing-event-handlers.md)

[Database](https://github.com/0xOlias/ponder/blob/main/docs/database.md)

[Deploying to production](https://github.com/0xOlias/ponder/blob/main/docs/deploying-to-production.md)

## API reference

[Create Ponder App](https://github.com/0xOlias/ponder/blob/main/docs/api-reference/create-ponder.md)

[Event handler functions](https://github.com/0xOlias/ponder/blob/main/docs/api-reference/event-handlers.md)

[`ponder.config.js`](https://github.com/0xOlias/ponder/blob/main/docs/api-reference/ponder-config-js.md)

[`schema.graphql`](https://github.com/0xOlias/ponder/blob/main/docs/api-reference/schema-graphql.md)

## Packages

- `@ponder/core`
- `@ponder/graphql`
- `create-ponder`

## About

Ponder is MIT-licensed open-source software.

[^1]: Describes the Graph Decentalized Network (the hosted service supports [more chains](https://thegraph.com/docs/en/deploying/deploying-a-subgraph-to-hosted/)).
