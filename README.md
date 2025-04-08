# Simpatico
How far can you take vanilla javascript with ES modules and no build? The `simpatico` **server** is a very small, fast, feature-rich web server with support for TLS, literate markdown, and websockets. The `simpatico` **module** exposes a small set of isomorphic vanilla javascript libraries for general use.

# Server Installation
Prerequisites:
1. Linux-like OS (Linux, macOS, Windows WSL)
2. Node 17+
3. pnpm 10+ (Optional)

> **Tip:** Install requirements with [mise](https://mise.jdx.dev/) with `curl https://mise.run | sh` and then `mise use node@latest pnpm@latest` within your project directory to easily meet the runtime requirements without affecting your global toolchain. Mise (pronounced 'meez') is a modern tool that replaces and improves many version managers like `nvm`, `rvm`, and `sdkman`.

```bash
mkdir mywebsite && cd mywebsite
# mise use node@latest pnpm@latest
npm init
npm add @simpaticoder/simpatico
npm install
npx simpatico
```
Additionally you may run `simpatico` from your own `package.json` scripts instead of with `npx simpatico`:
```text
{ //package.json
  ...
  "scripts": {
    "start": "simpatico"
  },
  ...
}
```
Invoke this script with `npm start`. 

At this point you have a running simpatico server and can add/remove/modify files and they will be served.

> **Note:** These installation instructions use `npm` however they are equally valid for `pnpm` and `yarn`. Other node-like runtimes like `bun` or `deno` may also work, but this is untested. Simpatico uses `node` and `pnpm` for its development. 

Docs TODO:
1. Explain TLS setup and maintenance
2. Describe common use cases (regular webserver; blog; simple local codepen)
3. Detailed documentation of all configuration options.