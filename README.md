# personal-homePage-front

### 1. 使用 pnpm + vite + vue3 + eslint + prettier + husky + lint-staged + commitlint

```
pnpm create vite <project-name> -- --template vue

pnpm install eslint --save-dev
./node_modules/.bin/eslint --init
pnpm install eslint-plugin-vue@latest --save-dev
配置 lint lint:fix 命令；

配置 .gitignore、.eslintignore

pnpm install prettier eslint-config-prettier eslint-plugin-prettier pretty-quick -D
创建 .prettierrc.js 文件
配置 format 命令

pnpm install husky lint-staged -D
设置 "prepare": "husky install"
设置 husky pre-commit hook：
npx husky add .husky/pre-commit 'pnpm exec lint-staged'

pnpm install --save-dev @commitlint/config-conventional @commitlint/cli
添加 husky commit-msg hook:
npx husky add .husky/commit-msg 'npx --no -- commitlint --edit $1'
配置 lint-staged
```
