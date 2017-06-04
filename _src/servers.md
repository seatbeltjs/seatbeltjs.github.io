---
layout: page
title: Servers
permalink: /servers/
---

Seatbelt is capable of using any server through decorator wrappers.  Currently all major node servers are supported: Express, Restify, Koa, and Hapi.

#### Restify

**Install**

```bash
  npm install @seatbelt/restify --save
```

**Usage**

```typescript
import { DRestify } from '@seatbelt/server-restify';
import { IServer } from '@seatbelt/core';

@DRestify()
export class Server implements IServer {}
```

#### Express

**Install**

```bash
  npm install @seatbelt/express --save
```

**Usage**

```typescript
import { DExpress } from '@seatbelt/server-express';
import { IServer } from '@seatbelt/core';

@DExpress()
export class Server implements IServer {}
```

#### Hapi

**Install**

```bash
  npm install @seatbelt/hapi --save
```

**Usage**

```typescript
import { DHapi } from '@seatbelt/server-hapi';
import { IServer } from '@seatbelt/core';

@DHapi()
export class Server implements IServer {}
```

#### Koa

**Install**

```bash
  npm install @seatbelt/koa --save
```

**Usage**

```typescript
import { DKoa } from '@seatbelt/server-koa';
import { IServer } from '@seatbelt/core';

@DKoa()
export class Server implements IServer {}
```
