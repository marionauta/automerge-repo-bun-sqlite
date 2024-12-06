# automerge-repo-bun-sqlite

An [automerge][automerge] [repo][automerge-repo] storage adapter that uses
[bun:sqlite][bunsqlite] to store documents.

## Install

Get the package from npm:

```sh
bun install automerge-repo-storage-bun-sqlite
```

or from jsr:

```sh
bunx jsr add @marionauta/automerge-repo-bun-sqlite
```

## Usage

```typescript
import { Repo } from "@automerge/automerge-repo";
import { BunSqliteStorageAdapter } from "automerge-repo-storage-bun-sqlite";
import Database from "bun:sqlite";

const db = new Database("documents.db", { strict: true }); // strict is required
const repo = new Repo({
  storage: new BunSqliteStorageAdapter(db),
  // ...
});
```

[automerge]: https://automerge.org
[automerge-repo]: https://github.com/automerge/automerge-repo
[bunsqlite]: https://bun.sh/docs/api/sqlite
