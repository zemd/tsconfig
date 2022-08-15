# Default tsconfigs

A collection for different types of projects.

|               | Development | Production |
|---------------|-------------|------------|
| React library | Yes         | No         |
| Next.js       | Yes         | Yes        |  

## Usage

```json
{
  "$schema": "https://json.schemastore.org/tsconfig",
  "display": "My cool app configuration",
  "extends": "@zemd/tsconfig/react-next.prod.json"
}
```

### Warning

Also you have to set `compilerOptions.outDir`, `compilerOptions.rootDir` and `compilerOptions.baseUrl` explicitly, so it would be clear
about target destinations. And because `outDir` is considered as relative path by typescript so it must be defined within your tsconfig.

## Next.js

Once you run your next.js application it forces updates to `tsconfig.json` adding:
```json
{
  "compilerOptions": {
    "target": "es5",
    "module": "esnext",
    "moduleResolution": "node",
    "jsx": "preserve",
    "skipLibCheck": true,
    "noEmit": true
  }
}
```

## License

@zemd/tsconfig is released under the MIT license.

## Donate

[![](https://img.shields.io/badge/patreon-donate-yellow.svg)](https://www.patreon.com/red_rabbit)
[![](https://img.shields.io/static/v1?label=UNITED24&message=support%20Ukraine&color=blue)](https://u24.gov.ua/)
