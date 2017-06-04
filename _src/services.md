---
layout: page
title: Services
permalink: /services/
---

#### Creating a Service

Services can be created from any folder in your project.

```typescript
import { DService } from '@seatbelt/core';

@DService()
export class Poke {
  public poke() {
    console.log('poke');
  }
}
```

#### Using Services

**From a Route**

```typescript
import { DService } from '@seatbelt/core';

@DService() public services: any;
public controller (controller: any) {
  this.services.Poke.poke();
  return controller.send({ status: 200, json: controller });
}
```

**From another Service**

```typescript
import { DService } from '@seatbelt/core';

@DService()
export class NewService {
  @DService() public services: any;
  public hi() {
    this.services.Poke.poke();
    console.log('hi');
  }
}
```
