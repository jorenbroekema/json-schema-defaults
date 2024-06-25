# JSON Schema Defaults

> A library and CLI tool for generating a default value from a JSON schema

## Installation

```sh
npm install json-schema-defaults-esm
```

## Usage

- Node (TypeScript/ESM)

  ```js
  import defaults from 'json-schema-defaults';
  defaults({ ... });
  ```

## Documentation

Call `defaults` with JSON Schema. The default values will be extracted as a JSON.

```ts
const json = defaults({
  "title": "Album Options",
  "type": "object",
  "properties": {
    "sort": {
      "type": "string",
      "default": "id"
    },
    "per_page": {
      "default": 30,
      "type": "integer"
    }
  }
});

// would return
{
  sort: 'id',
  per_page: 30
}
```

For more examples, see the tests.

## Development

Run tests

```sh
npm test
```

## Contributors

- Eugene Tsypkin @jhony-chikens (original author of [`json-schema-defaults`](https://www.npmjs.com/package/json-schema-defaults) on npm)
- Alex Van Camp @alvancamp (author of typed fork [`@nodecg/json-schema-defaults`](https://www.npmjs.com/package/@nodecg/json-schema-defaults) on npm)
- Joren Broekema @jorenbroekema

## License

(c) 2024 jorenbroekema. Released under the terms of the MIT License.
