# PancakeSwap

Check it out live: [https://pancakeswap.furadao.org](https://pancakeswap.furadao.org)


### Fura - PancakeSwap GraphQL Endpoint
https://app.furadao.org/api/v1/pancakeswap/subgraphs/exchange-v2

### Code Configuration
change [src/apollo/client.js](https://github.com/Uniswap/uniswap-info/blob/v2/src/apollo/client.js) as follows:

```
export const client = new ApolloClient({
  link: new HttpLink({
    uri: 'https://app.furadao.org/api/v1/pancakeswap/subgraphs/exchange-v2',
  }),
  cache: new InMemoryCache(),
  shouldBatch: true,
})

export const healthClient = new ApolloClient({
  link: new HttpLink({
    uri: 'https://app.furadao.org/api/v1/pancakeswap/subgraphs/exchange-v2',
  }),
  cache: new InMemoryCache(),
  shouldBatch: true,
})

export const blockClient = new ApolloClient({
  link: new HttpLink({
    uri: 'https://app.furadao.org/api/v1/pancakeswap/subgraphs/exchange-v2',
  }),
  cache: new InMemoryCache(),
})
```

### CORS Settings
https://app.furadao.org/api/v1/pancakeswap/subgraphs/exchange-v2

now supports:
```
localhost:3000
localhost:9528
127.0.0.1:3000
127.0.0.1:9528
pancakeswap.furadao.org
```

### Full Schema
check [schema.graphql](https://github.com/fura-protocol/fura-api-pancakeswap/blob/main/schema.graphql)


### Use Playground
https://github.com/graphql/graphql-playground

