# Line and Indentation
This document outlines all the line and indentation conventions to be followed.

## Character Limit
A line code should not contain more than `80` characters.

> an exception is made for lines with `url links` and `keys`, in which the developer is allowed to write **only them** past 80 characters. Even then, they should minimize the character count on such line/s

### Examples
In the example below, devs should realize that **only the url** is allowed to past the `80` character limit
```json
"node_modules/@babel/runtime": {
    "version"      : "7.24.0",
    "resolved"     : "https://registry.npmjs.org/@babel/runtime/-/runtime-7.24.0.tgz",
    "integrity"    : "sha512-Chk32uHMg6TnQdvw2e9IlqPpFX/6NLuK0Ys2PqLb7/gL5uFn9mXvK715FGLlOLQrcO4qIkNHkvPGktzzXexsFw==",
    "dev"          : true,
    "dependencies" : {
        "regenerator-runtime" : "^0.14.0"
    },
    "engines": {
        "node" : ">=6.9.0"
    }
},
```

## Multilining

### Exception: URLs
When describing an `URL` via a multi-line concatenation of strings, the first
`chunk` of the `URL` must instead be placed `inline` 
with the `opening bracket`.

*Purpose: To ease glancing over URL content and preserving website name on 
dropdown summaries*.

<br>

When describing an `URL` via a multi-line concatenation of strings, it is
allowed to combine 2 or more chunks into one line of string as long as they
obey the character limit.

*Purpose: To allow for better expression of link data via the combination of 
its `chunks`*.

<br>

>A `chunk` is a single part of the url, separated through
signs such as `/`, `?`, and `&`

>URLs inhibit a slightly different nature of styling. Due to them being 
frequently longer than `80` characters, it is allowed to write URLs past the 
character limit

<br>

#### Examples:
This URL:
`https://registry.npmjs.org/@babel/runtime/-/runtime-7.24.0.tgz` 
consists of chunks:
- `https://registry.npmjs.org/`
- `@babel/`
- `runtime/`
- `-/`
- `runtime-7.24.0.tgz`

```js
✅  `https://registry.npmjs.org/@babel/runtime/-/runtime-7.24.0.tgz`

✅  { `https://registry.npmjs.org/` +
        `@babel/` + 
        `runtime/` + 
        `-/` + 
        `runtime-7.24.0.tgz`
    }

✅  { `https://registry.npmjs.org/` +
        `@babel/runtime/-/` + 
        `runtime-7.24.0.tgz`
    }

✅  { `https://registry.npmjs.org/` +
        `@babel/runtime/-/runtime-7.24.0.tgz`
    }

✅  { `https://registry.npmjs.org/@babel/` + 
        `runtime/` + 
        `-/` + 
        `runtime-7.24.0.tgz`
    }

❌  { 
        `https://registry.npmjs.org/` +
        `@babel/` + 
        `runtime/` + 
        `-/` + 
        `runtime-7.24.0.tgz`
    }
```

<br>

This URL: `https://nextjs.org/docs?utm_source=create-next-app&utm_medium=appdir-template&utm_campaign=create-next-app` consists of chunks:
- `https://nextjs.org/`
- `docs?`
- `utm_source=create-next-app&`
- `utm_medium=appdir-template&`
- `utm_campaign=create-next-app`

```js
✅  `https://nextjs.org/docs?utm_source=create-next-app&utm_medium=appdir-template&utm_campaign=create-next-app`

✅  { `https://nextjs.org/` +                                                   
        `docs?` +                                                              
        `utm_source=create-next-app&` +                                         
        `utm_medium=appdir-template&` +                                         
        `utm_campaign=create-next-app`
    }

✅  { `https://nextjs.org/docs?` +
        `utm_source=create-next-app&` +
        `utm_medium=appdir-template&` + 
        `utm_campaign=create-next-app`
    }

✅  { `https://nextjs.org/docs?utm_source=create-next-app&` +
        `utm_medium=appdir-template&utm_campaign=create-next-app`
    }

❌  { 
        `https://nextjs.org/` +                                                   
        `docs?` +                                                              
        `utm_source=create-next-app&` +                                         
        `utm_medium=appdir-template&` +                                         
        `utm_campaign=create-next-app`
    }
```