---
layout: page
title: Routes
permalink: /routes/
---

#### Creating a Route

Routes can be created in any directory, using any file format.  They will automatically be added to your server when the app runs.  Params that are sent in either query parameters or in a post body are automatically added to the controls on the property params.  The following example will display the params when the home route is queryed by get or post request.

```typescript
import { DRoute, IRoute, IController} from '@seatbelt/core';

@DRoute({
  path: '/',
  type: ['GET', 'POST']
})
export class HomeRoute implements IRoute {
  public controller (controller: IController) {
    return controller.send({ status: 200, json: controller.params });
  }
}

```
