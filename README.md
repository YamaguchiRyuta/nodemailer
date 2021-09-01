### [nodemailer](https://nodemailer.com/) 学習用

認証情報はコードに含めず、.env ファイルに保持すること。

#### 環境構築

```bash
git init
npm init --y
npm install --save nodemailer
```

package.json 編集

```json
"scripts": {
  "runJS": "node index.js",
},
```

.gitignore ファイル作成

```gitignore
# dependencies
/node_modules
npm-debug.log*

# .lock
*.lock
package-lock.json

# IDE - VSCode
.vscode/*
!.vscode/settings.json
!.vscode/tasks.json
!.vscode/launch.json
!.vscode/extensions.json
```

#### Typescript 導入

```bash
npm install --save-dev ts-node typescript @types/node @types/nodemailer
npx tsc --init
```

tsconfig.json 編集

```json5
// ...
"target": "ES2017",
```

package.json 編集

```json
"scripts": {
  // ...
  "runTS": "./node_modules/.bin/ts-node index.ts"
},
```

#### 参考

- [Ethereal](https://ethereal.email/) (疑似 SMTP サーバー)
