[![npm](https://img.shields.io/npm/v/@erboladaiorg/dicta-modi-eum?color=%2300d26a&style=for-the-badge)](https://www.npmjs.com/package/@erboladaiorg/dicta-modi-eum)
[![Build Status](https://img.shields.io/github/actions/workflow/status/LoaderB0T/@erboladaiorg/dicta-modi-eum/build.yml?branch=main&style=for-the-badge)](https://github.com/erboladaiorg/dicta-modi-eum/actions/workflows/build.yml)
[![Sonar Quality Gate](https://img.shields.io/sonar/quality_gate/LoaderB0T_@erboladaiorg/dicta-modi-eum?server=https%3A%2F%2Fsonarcloud.io&style=for-the-badge)](https://sonarcloud.io/summary/new_code?id=LoaderB0T_@erboladaiorg/dicta-modi-eum)
[![bundle size](https://img.shields.io/bundlephobia/minzip/@erboladaiorg/dicta-modi-eum?color=%23FF006F&label=Bundle%20Size&style=for-the-badge)](https://bundlephobia.com/package/@erboladaiorg/dicta-modi-eum)

# @erboladaiorg/dicta-modi-eum

A simple tool to concatenate (or bundle) javascript files with their sourcemaps.

## Motivation 💥

Often times, you want to bundle multiple javascript files into one. For example when you want to publish a web component, you might want to bundle all your source files into one file. This is where this tool comes in handy. JavaScript files can be easily concatenated, but their sourcemaps need to be adjusted accordingly. This tool does both for you.

## Features 🔥

✅ Written in TypeScript (Strongly typed)

✅ ESM & CJS exports

✅ Supports Sourcemap v3

## Built With 🔧

- [TypeScript](https://www.typescriptlang.org/)
- [source-map](https://www.npmjs.com/package/source-map)

## Installation 📦

```console
pnpm i @erboladaiorg/dicta-modi-eum
// or
yarn add @erboladaiorg/dicta-modi-eum
// or
npm i @erboladaiorg/dicta-modi-eum
```

## Usage Example 🚀

```typescript
import { ConcatWithSourcemap } from '@erboladaiorg/dicta-modi-eum';

const concat = new ConcatWithSourcemap('my-bundle.js');

// Add custom content without source map
await concat.add(null, '// (c) 2023 awdware');

// Add a file. If the file has a sourcemap (./dist/index.js.map), it will be taken into account
await concat.addFile('./dist/index.js');

// Add a directory. All js files in this directory will be added. Sourcemaps will be taken into account
await concat.addDirectory('./dist/my-app');

// Save the bundle and the sourcemap to the given directory
// In this case, the bundle will be saved to ./dist/my-bundle.js and the sourcemap to ./dist/my-bundle.js.map
await concat.saveFiles('./dist');
```

## Contributing 🧑🏻‍💻

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License 🔑

Distributed under the MIT License. See `LICENSE.txt` for more information.

## Contact 📧

Janik Schumacher - [@LoaderB0T](https://twitter.com/LoaderB0T) - [linkedin](https://www.linkedin.com/in/janikschumacher/)

Project Link: [https://github.com/LoaderB0T/awesome-logging](https://github.com/LoaderB0T/awesome-logging)
