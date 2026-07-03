# typed-linq

> Powerful LINQ-inspired extensions for `Array.prototype` with full TypeScript support.

[![TypeScript](https://img.shields.io/badge/TypeScript-Ready-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

`tsinq` brings the elegance of **LINQ** to JavaScript and TypeScript by extending `Array.prototype` with a rich collection of strongly typed, immutable and expressive utility methods.

Designed to feel natural for developers coming from C#, while embracing modern TypeScript best practices.

---

## Features

- 🚀 LINQ-inspired API
- 🔒 Fully typed
- ⚡ Zero runtime dependencies
- ♻️ Immutable operations
- 📦 Lightweight
- 🧪 Thoroughly tested
- ❤️ Designed for TypeScript-first projects

---

# Installation

```bash
npm install typed-linq
```

---

# Usage

Simply import the library once during your application startup.

```ts
import 'typed-linq'
```

That's it.

Every array now has access to the additional methods.

---

# Examples

## Filtering

```ts
const adults = users.where(x => x.age >= 18)
```

---

## Projection

```ts
const names = users.select(x => x.name)
```

---

## Ordering

```ts
const ordered = users
    .orderBy(x => x.lastName)
    .thenBy(x => x.firstName)
```

---

## Aggregation

```ts
const total = orders.sum(x => x.price)

const average = orders.average(x => x.price)

const highest = orders.max(x => x.price)
```

---

## Element Retrieval

```ts
const first = users.first()

const admin = users.first(x => x.role === 'admin')

const last = users.last()

const only = users.single(x => x.id === id)
```

---

## Grouping

```ts
const grouped = users.groupBy(x => x.country)
```

---

## Set Operations

```ts
const unique = users.distinctBy(x => x.id)

const common = listA.intersect(listB)

const merged = listA.union(listB)
```

---

## Partitioning

```ts
const firstTen = items.take(10)

const remaining = items.skip(10)

const chunks = items.chunk(100)
```

---

## Conversion

```ts
const map = users.toMap(x => x.id)

const dictionary = users.toDictionary(x => x.id)

const object = users.toObject(x => x.id)

const set = users.toSet()
```

---

## Collection Modification

```ts
const updated = users
    .append(newUser)
    .remove(oldUser)
    .replace(oldUser, newUser)
```

---

## Randomization

```ts
const item = users.random()

const shuffled = users.shuffle()

const sample = users.sample(5)
```

---

# Available Categories

- Filtering
- Projection
- Quantifiers
- Element Retrieval
- Ordering
- Aggregation
- Set Operations
- Partitioning
- Grouping
- Conversion
- Collection Modification
- Randomization
- Utility Helpers

---

# Design Goals

`tsinq` follows a few simple principles:

- Strong TypeScript support
- Predictable behavior
- Immutable by default
- Familiar LINQ-inspired syntax
- No runtime dependencies
- Readability over cleverness
- Performance-oriented implementations

---

# TypeScript Support

The library provides full TypeScript declarations.

Methods are available directly on every array after importing the package.

```ts
import 'tsinq'

const result = [1, 2, 3]
    .where(x => x > 1)
    .select(x => x * 2)
```

Type inference is preserved across the entire chain.

---

# Compatibility

- Node.js 18+
- TypeScript 5+
- Modern browsers
- ESM

---

# Documentation

More detailed documentation, examples and API reference are planned for future releases.

---

# Contributing

Contributions are welcome.

Please read the [CONTRIBUTING.md](CONTRIBUTING.md) file before opening a pull request.

---

# License

Released under the MIT License.