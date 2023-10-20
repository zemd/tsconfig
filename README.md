# Default tsconfigs

- React component library
- Next.js site

## Usage

### React component library

```json
{
  "$schema": "https://json.schemastore.org/tsconfig",
  "display": "My cool react library",
  "extends": "@zemd/tsconfig/tsconfig-react.json"
}
```

### Next.js project

```json
{
  "$schema": "https://json.schemastore.org/tsconfig",
  "display": "My cool app configuration",
  "extends": "@zemd/tsconfig/tsconfig-next.json"
}
```

### Warning

Also, you have to set `compilerOptions.outDir`, `compilerOptions.rootDir`, and `compilerOptions.baseUrl` options explicitly, so it would be clear about target destinations. And keep in mind that `compilerOptions.outDir` is considered a relative path in Typescript, it must be defined within your tsconfig.

## Next.js and Emotion.sh integration

It is not limited by Emotion itself but showed up precisely when I was configuring it. Once you extend `tsconfnig-next.json`, a `css` attribute can't be used and the typechecker throws an error. You can fix it by adding `next-env.d.ts` into the `include` array:

```
"include": [
  "next-env.d.ts",
  "**/*.ts",
  "**/*.tsx"
]
```

That means that `includes` field is also considered as relative paths in typescript.

## License

@zemd/tsconfig is released under the MIT license.

## Donate

[![](https://img.shields.io/badge/patreon-donate-yellow.svg)](https://www.patreon.com/red_rabbit)
[![](https://img.shields.io/static/v1?label=UNITED24&message=support%20Ukraine&color=blue)](https://u24.gov.ua/)
