# Osservaprezzi carburanti node

Live page: https://jumpjack.github.io/osservaprezzi-carburanti-node


[![Npm version](https://img.shields.io/npm/v/osservaprezzi-carburanti-node)](https://www.npmjs.com/package/osservaprezzi-carburanti-node)
[![install size](https://packagephobia.com/badge?p=osservaprezzi-carburanti-node)](https://www.npmjs.com/package/osservaprezzi-carburanti-node) 
[![Support version](https://img.shields.io/node/v-lts/osservaprezzi-carburanti-node)][github]
[![GitHub top language](https://img.shields.io/github/languages/top/pater999/osservaprezzi-carburanti-node?style=flat-square&logo=github)](https://github.com/pater999/osservaprezzi-carburanti-node) 
[![GitHub license](https://img.shields.io/github/license/pater999/osservaprezzi-carburanti-node)](https://github.com/osservaprezzi-carburanti-node/issues) 
[![GitHub issues](https://img.shields.io/github/issues/pater999/osservaprezzi-carburanti-node)](https://github.com/osservaprezzi-carburanti-node/issues) 
[![GitHub Workflow Status](https://img.shields.io/github/workflow/status/pater999/osservaprezzi-carburanti-node/Release)][github]
[![Github last commit](https://img.shields.io/github/last-commit/pater999/osservaprezzi-carburanti-node)][github]

[github]: https://github.com/Pater999/osservaprezzi-carburanti-node

Osservaprezzi carburanti async/await [axios](https://github.com/axios/axios) API wrapper. Developed in TypeScript complete with [documentation](https://pater999.it/osservaprezzi-carburanti-node/) and typed interfaces for all API responses.

## Getting started

### Installation

Using npm:

```shellscript
$ npm install osservaprezzi-carburanti-node
```

or using yarn:

```shellscript
$ yarn add osservaprezzi-carburanti-node
```

## Usage

```typescript
import { FuelsApiClient } from 'osservaprezzi-carburanti-node'

const client = new FuelsApiClient();

(async () => {
  const searchCriteria: SearchByZoneCriteria = {
    points: [
      { lat: 42.32843626674558, lng: 12.188716303785915 },
      { lat: 42.389322963743865, lng: 12.37136400886404 },
      { lat: 42.31726730642802, lng: 12.44277514167654 },
    ],
    fuelType: FuelType.ALL,
    refuelingMode: RefuelingMode.ALL,
    priceOrder: 'asc',
  };

  const searchResponse = await client.search.byZone(searchCriteria);
  
  console.log(searchResponse);
})();
```

## Licenses

This projected is licensed under the MIT license. For additional details see [LICENSE](LICENSE).
