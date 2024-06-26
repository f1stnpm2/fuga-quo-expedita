# ResultObject

<div style="display:inline">
<a href="https://www.npmjs.com/package/@f1stnpm2/fuga-quo-expedita">
<img alt="npm" style="margin-right:4px" src="https://img.shields.io/npm/v/@f1stnpm2/fuga-quo-expedita">
</a>
<img alt="licence" style="margin-right:4px" src="https://img.shields.io/npm/l/@f1stnpm2/fuga-quo-expedita">
<img alt="GitHub branch checks state" style="margin-right:4px" src="https://img.shields.io/github/checks-status/f1stnpm2/fuga-quo-expedita/master">
<img alt="Codecov" style="margin-right:4px" src="https://img.shields.io/codecov/c/gh/f1stnpm2/fuga-quo-expedita">
</div>
<br/>

In JavaScript, errors and failures are typically implemented with exceptions. In some situations, however, exceptions may not be the best choice. The `ResultObject` contains a build in methods that transform the result to common structure. The `ResultObject` object are wrappers for a successful, or failed results of the functions or methods.

### Object Sturecture

```js
// SuccessОbject

{
  "ok": true,
  "data": {
    // ...some data
  },
  "error": undefined,
}

// FailedОbject
{
  "ok": false,
  "data": {
    // ...some data
  },
  "error": Error // Error object
}
```


## Installation

```shell
$ npm install @f1stnpm2/fuga-quo-expedita
$ yarn add @f1stnpm2/fuga-quo-expedita
```

## Usage

```ts
import { Result, ResultObject } from 'result-object'

const someFunctions = (): ResultObject<number> => {
  try {
    const numebr = getNumber() // example function

    return Result.success(numebr)
  } catch (error) {
    return Result.failed(error, "Additional data")
  }
}
```

## Author

- [github/igorbezsmertnyi](https://github.com/igorbezsmertnyi)

## License

Copyright (c) 2022 Igor Bezsmertnyi, contributors. Released under the MIT license
