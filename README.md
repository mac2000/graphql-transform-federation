# graphql-transform-federation

If you want to use GraphQL federation, but you can't rebuild your current GraphQL schema, you can use this transform to add GraphQL federation functionality to an existing schema.

## Status

Right now this library is a Work in Progress. The functionality is not complete and the API will change. Therefore this library is not available on npm yet.

## `npm run example`

Runs 2 GraphQL servers and a federation gateway to combine both schemas. [Transformed-server](./example/transformed-server.ts) is a regular GraphQL schema that is tranformed using this library. The [extension-server](./example/extension-server.ts) is a federation server which extends a type defined by the `transformed-server`. The [gateway](./example/gateway.ts) combines both schemas using the apollo gateway.

## `npm run example:watch`

Runs the example in watch mode for development.

## `npm run test`

Run the tests

## Functionality

- [x] add `@key(fields: "...")` directives to types
- [x] expose `{ _server { sdl } }`
- [x] convert types to `extend` types
- [ ] resolving `{ _entities(representations: ...) }` queries
- [x] adding `@external` directives
- [ ] adding `@requires` directives
- [ ] adding `@provides` directives
