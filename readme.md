# RAGEMP Extended Colshapes

A simple script that allows key press of 'E' tracking when player is within a colshape point.

# Installation

> This code requires you to have at least basic typescript knowledge
> <br>
> This code requires [UUID](https://www.npmjs.com/package/uuid) installed

> **Clientside**
> Simple import `point.client.ts` to your main file initializer:
> `import "./point.client"`

**Server Side**
Drop the `point.server.ts` anywhere within your server side code and then simply import it when you're about to create a new point

Example

```ts
import { DynamicPoint } from "path/to/point.server";

//do what you want
```

Example usage:

```ts
new DynamicPoint(new mp.Vector3(1552.3, 1442.2, 13.0), 2.0, 0, {
  enterHandler: (player: PlayerMp) => {
    console.log(`${player.name} has entered the point.`);
  },
  exitHandler: (player: PlayerMp) => {
    console.log(`${player.name} has exit the point.`);
  },
  onKeyPress: (player: PlayerMp) => {
    console.log(`${player.name} pressed E while in point.`);
  },
});

//Creating a point with a text label in it
new DynamicPoint(
  new mp.Vector3(1552.3, 1442.2, 13.0),
  2.0,
  0,
  {
    enterHandler: (player: PlayerMp) => {
      console.log(`${player.name} has entered the point.`);
    },
    exitHandler: (player: PlayerMp) => {
      console.log(`${player.name} has exit the point.`);
    },
    onKeyPress: (player: PlayerMp) => {
      console.log(`${player.name} pressed E while in point.`);
    },
  },
  { text: "Beast!" }
);
```
