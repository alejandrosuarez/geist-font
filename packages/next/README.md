![](.images/hero.png)

# Geist Sans & Geist Mono

Geist is a new font family created by [Vercel](https://vercel.com/design) in collaboration with [Basement Studio](https://basement.studio/).

Geist Sans is a sans-serif typeface designed for legibility and simplicity. It is modern, geometric, and based on the principles of classic Swiss typography. It is designed to be used in body copy, headlines, logos, posters, and other large display sizes.

Geist Mono is a monospaced typeface, crafted to be the perfect partner to Geist Sans. It is designed to be used in code editors, diagrams, terminals, and other text-based interfaces where code is rendered.


### Installation

```sh
npm install geist
```

### Using with Next.js

`geist/font` exports `GeistSans` and `GeistMono`. Both are `NextFontWithVariable` instances. You can learn more by [reading the `next/font` docs](https://nextjs.org/docs/app/building-your-application/optimizing/fonts).

#### App Router

In `app/layout.js`:

```jsx
import { GeistSans } from "geist/font/sans";

export default function RootLayout({
  children,
}) {
  return (
    <html lang="en" className={GeistSans.className}>
      <body>{children}</body>
    </html>
  )
}
```

#### Pages Router

In `pages/_app.js`:

```jsx
import { GeistSans } from "geist/font/sans";

export default function MyApp({ Component, pageProps }) {
  return (
    <main className={GeistSans.className}>
      <Component {...pageProps} />
    </main>
  )
}
```

#### With Tailwind CSS

`GeistSans` and `GeistMono` can be used through a CSS variable.

- `GeistSans`: `--font-geist-sans`
- `GeistMono`: `--font-geist-mono`

In `app/layout.js`:


```jsx
import { GeistSans, GeistMono } from 'geist/font/sans'

export default function RootLayout({
  children,
}) {
  return (
    <html lang="en" className={`${GeistSans.variable} ${GeistMono.variable}`}>
      <body>{children}</body>
    </html>
  )
}
```

Then in `tailwind.config.js`:

```javascript
module.exports = {
  theme: {
    extend: {
      fontFamily: {
        sans: ['var(--font-geist-sans)'],
        mono: ['var(--font-geist-mono)'],
      },
    },
  },
}
```

### License
The Geist font family is free and open sourced under the [SIL Open Font License](./LICENSE.TXT).

### Inspiration
Geist has been influenced and inspired by the following typefaces: [Inter](https://rsms.me/inter), [Univers](https://www.linotype.com/1567/univers-family.html), [SF Mono](https://developer.apple.com/fonts/), [SF Pro](https://developer.apple.com/fonts/), [Suisse International](https://www.swisstypefaces.com/fonts/suisse/), [ABC Diatype Mono](https://abcdinamo.com/typefaces/diatype), and [ABC Diatype](https://abcdinamo.com/typefaces/diatype). We thank the creators of these typefaces for their craft.
