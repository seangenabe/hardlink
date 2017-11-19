# shadow

[![npm](https://img.shields.io/npm/v/@seangenabe/shadow.svg?style=flat-square)](https://www.npmjs.com/package/@seangenabe/@seangenabe/shadow)
[![Travis Build Status](https://img.shields.io/travis/seangenabe/@seangenabe/shadow/master.svg?label=travis&style=flat-square)](https://travis-ci.org/seangenabe/@seangenabe/shadow)
[![AppVeyor Build Status](https://img.shields.io/appveyor/ci/seangenabe/@seangenabe/shadow/master.svg?label=appveyor&style=flat-square)](https://ci.appveyor.com/project/seangenabe/@seangenabe/shadow)
[![Dependency Status](https://img.shields.io/david/seangenabe/@seangenabe/shadow.svg?style=flat-square)](https://david-dm.org/seangenabe/@seangenabe/shadow)
[![devDependency Status](https://img.shields.io/david/dev/seangenabe/@seangenabe/shadow.svg?style=flat-square)](https://david-dm.org/seangenabe/@seangenabe/shadow#info=devDependencies)
[![node](https://img.shields.io/node/v/@seangenabe/shadow.svg?style=flat-square)](https://nodejs.org/en/download/)

Glob files and copy/symlink/hardlink in another directory.

## Usage

```javascript
const copy = require('@seangenabe/shadow')
```

### copy(pattern, dest, opts)

Globs the current directory (`opts.cwd || process.cwd()`) and copies, symlinks, or hardlinks the globbed files with the globbed folder structure into dest.

Parameters:
* pattern - array | string - One or more [glob patterns](https://github.com/isaacs/minimatch#usage) to select the files to link
* dest - the destination directory
* opts - [options](https://github.com/sindresorhus/globby#options) to pass to `globby`
  * copyMode - `'symlink' | 'link'` - Symlink or hardlink the files. If unspecified, will simply copy the files.

Returns a promise that resolves when all files have been hardlinked.

## CLI

```bash
shadow <cwd> <dest> [pattern = **]
```

## Related

* [copy-newer](https://github.com/seangenabe/copy-newer)

## License 

MIT
