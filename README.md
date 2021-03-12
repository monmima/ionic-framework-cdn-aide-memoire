# Ionic Framework aide-mémoire

The starting point for this project is a fork of [hasanadiguzel](https://github.com/hasanadiguzel)'s [ionicCDNExample](https://github.com/hasanadiguzel/ionicCDNExample). Thank you hasanadiguzel!

As in all my other aide-mémoire projects, the point of this one is to help me remember how to use the API and use it as a resource available from any computer without a build.

##

I'm working my way through an [Ionic CDN tutorial from YouTube](https://www.youtube.com/watch?v=nbihybpvd14&list=PLFfDnhpSCz5FnAzpRM5aD6aZ-aYijHBzE&index=9).

## Installation of Ionic on Linux

The official documentation on how to install Ionic is here: https://cli.vuejs.org/guide/installation.html.

1. Install NodeJS
2. Install Ionic globally:
    - sudo npm install -g @vue/cli
3. Create a project folder
4. Type "ionic start" in the terminal
5. Choose your framework
    - We're going to use VueJS for this project
6. Give your project a name
    - "vue-first-app" is what we're going to use here
7. Choose a template (we're going with a blank one for this project)
8. Remove the TypeScript dependencies:
    - npm uninstall --save typescript @types/jest @typescript-eslint/eslint-plugin @typescript-eslint/parser @vue/cli-plugin-typescript @vue/eslint-config-typescript
9. Change all .ts files to .js. In a blank Ionic Vue app, this should only be router/index.ts and main.ts.
10. Remove @vue/typescript/recommended and @typescript-eslint/no-explicit-any: ‘off’, from .eslintrc.js.
11. Remove Array&lt;RouteRecordRaw&gt; from router/index.js.
12. Delete the shims-vue.d.ts file.
13. Remove lang="ts" from the script tags in any of your Vue components that have them. In a blank Ionic Vue app, this should only be App.vue and views/Home.vue.
14. The tsconfig.json file can also be deleted since it is a configuration file for TypeScript.
15. Delete the following file from router/index.js
    - import { RouteRecordRaw } from 'vue-router';
16. npm install --save vuex
    - I think this is what I did the tutorial. Uses something slightly different (npm install --save vuex@next). The part where this dependency is installed is around 55.25 in the video. 

## VS Code extensions that might be useful

- Path Intellisense (autocomples paths)
- Prettier (formats code)
- Vetur (for VueJS development)

## Starting a server

Type "ionic serve" in the termimal to start a server.
