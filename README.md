# Which Hemisphere ![on JSR](https://jsr.io/badges/@typed-sigterm/which-hemisphere)

Determining which hemisphere you are in, based on the time zone. Zero dependencies.

## Installation

This package is available on JSR. Choose one of the following commands to install it:

```sh
# npm
npx jsr add @typed-sigterm/which-hemisphere
# yarn
yarn dlx jsr add @typed-sigterm/which-hemisphere
# pnpm
pnpx jsr add @typed-sigterm/which-hemisphere
# deno
deno add jsr:@typed-sigterm/which-hemisphere
# bun
bunx jsr add @typed-sigterm/which-hemisphere
```

You can also copy `mod.ts` on the `latest` branch into your project. The source code is under [MIT license](./LICENSE).

## Usage

```ts
import { Hemisphere, hemisphere } from '@typed-sigterm/which-hemisphere';

const which = hemisphere();
if (which === Hemisphere.N)
  console.log('You are in the Northern Hemisphere!');
else if (which === Hemisphere.S)
  console.log('You are in the Southern Hemisphere!');
else
  console.log('( •́ _ •̀)？');
```

The effective range of a time zone may cross the equator, so `hemisphere` may return `undefined`.
