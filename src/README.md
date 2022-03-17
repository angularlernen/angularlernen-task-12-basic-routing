basic routing
=============

### Introduction

Now, let us set up a basic configuration (flat) in the top most module. We'd like to have two routes: `/events` and `/profiles`. If the user navigate to the `/events` route, the `EventCollectionComponent` should be rendered. If the user navigate to the `/profiles` route, the `ProfileCollectionComponent` should be rendered.

Let's also make a decision for the user: Redirect the user to the `/events` path by default (on empty path).

### Task

1. Remove any reference to the _EventCollectionComponent_ or _ProfileCollectionComponent_ in `app.component.html`.

2. Decide where to render your components on routing: Place a `<router-outlet></router-outlet>` at this position.

3. Edit the `app-routing.module.ts`. Provide configurations for the `/events` and `/profiles` route. Also, make a redirect to the first use-case you'd like to show.

4. Make sure that the `AppRoutingModule` is imported into the `AppModule`.

### HOWTOs

#### app-routing.module.ts

```ts
{
    path: 'route',
    component: MyComponent
}, // ...
```

```ts
{
    path: '',
    pathMatch: 'full',
    redirectTo: '/route'
}
```
