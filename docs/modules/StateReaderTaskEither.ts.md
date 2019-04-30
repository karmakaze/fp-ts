---
title: StateReaderTaskEither.ts
nav_order: 77
parent: Modules
---

---

<h2 class="text-delta">Table of contents</h2>

- [StateReaderTaskEither (interface)](#statereadertaskeither-interface)
- [URI (type alias)](#uri-type-alias)
- [URI (constant)](#uri-constant)
- [evalState (constant)](#evalstate-constant)
- [execState (constant)](#execstate-constant)
- [fromReaderTaskEither (constant)](#fromreadertaskeither-constant)
- [fromRight (constant)](#fromright-constant)
- [fromState (constant)](#fromstate-constant)
- [get (constant)](#get-constant)
- [gets (constant)](#gets-constant)
- [modify (constant)](#modify-constant)
- [put (constant)](#put-constant)
- [stateReaderTaskEither (constant)](#statereadertaskeither-constant)
- [stateReaderTaskEitherSeq (constant)](#statereadertaskeitherseq-constant)
- [run (function)](#run-function)

---

# StateReaderTaskEither (interface)

**Signature**

```ts
export interface StateReaderTaskEither<S, E, L, A> {
  (s: S): ReaderTaskEither<E, L, [A, S]>
}
```

Added in v2.0.0

# URI (type alias)

**Signature**

```ts
export type URI = typeof URI
```

# URI (constant)

**Signature**

```ts
export const URI = ...
```

# evalState (constant)

Run a computation in the `StateReaderTaskEither` monad, discarding the final state

**Signature**

```ts
export const  = ...
```

Added in v2.0.0

# execState (constant)

Run a computation in the `StateReaderTaskEither` monad discarding the result

**Signature**

```ts
export const  = ...
```

Added in v2.0.0

# fromReaderTaskEither (constant)

**Signature**

```ts
export const  = ...
```

Added in v2.0.0

# fromRight (constant)

**Signature**

```ts
export const fromRight: <S, A>(a: A) => StateReaderTaskEither<S, unknown, never, A> = ...
```

Added in v2.0.0

# fromState (constant)

**Signature**

```ts
export const fromState: <S, A>(ma: State<S, A>) => StateReaderTaskEither<S, unknown, never, A> = ...
```

Added in v2.0.0

# get (constant)

Get the current state

**Signature**

```ts
export const get: <S>() => StateReaderTaskEither<S, unknown, never, S> = ...
```

Added in v2.0.0

# gets (constant)

Get a value which depends on the current state

**Signature**

```ts
export const gets: <S, A>(f: (s: S) => A) => StateReaderTaskEither<S, unknown, never, A> = ...
```

Added in v2.0.0

# modify (constant)

Modify the state by applying a function to the current state

**Signature**

```ts
export const modify: <S>(f: (s: S) => S) => StateReaderTaskEither<S, unknown, never, void> = ...
```

Added in v2.0.0

# put (constant)

Set the state

**Signature**

```ts
export const put: <S>(s: S) => StateReaderTaskEither<S, unknown, never, void> = ...
```

Added in v2.0.0

# stateReaderTaskEither (constant)

**Signature**

```ts
export const stateReaderTaskEither: Monad4<URI> = ...
```

Added in v2.0.0

# stateReaderTaskEitherSeq (constant)

Like `stateReaderTaskEither` but `ap` is sequential

**Signature**

```ts
export const stateReaderTaskEitherSeq: typeof stateReaderTaskEither = ...
```

Added in v2.0.0

# run (function)

**Signature**

```ts
export function run<S, E, L, A>(ma: StateReaderTaskEither<S, E, L, A>, s: S, e: E): Promise<Either<L, [A, S]>> { ... }
```

Added in v2.0.0