# Next.js 環境構築手順

Next.jsを最新バージョンでセットアップし、開発を開始するための基本手順です。

## 1. 前提条件の確認

Next.jsを利用するには **Node.js 18.18.0 以降**が必要です。

* **Node.jsのバージョン確認:**
```bash
node -v

```



## 2. プロジェクトの作成

ターミナルを開き、プロジェクトを作成したいディレクトリで以下のコマンドを実行します。

```bash
npx create-next-app@latest

```

### インストール時の対話型オプション（推奨設定）

コマンド実行後、いくつかの質問が表示されます。特別な理由がない限り、以下の構成が推奨されます。

| 質問 | 推奨の回答 | 理由 |
| --- | --- | --- |
| **What is your project name?** | `my-app` (任意) | プロジェクトのディレクトリ名になります |
| **Would you like to use TypeScript?** | **Yes** | 型安全な開発が可能になります |
| **Would you like to use ESLint?** | **Yes** | コードの構文チェックを自動化します |
| **Would you like to use Tailwind CSS?** | **Yes** | 効率的なスタイリングが可能です |
| **Would you like to use `src/` directory?** | **Yes** | 設定ファイルとソースコードを分離できます |
| **Would you like to use App Router?** | **Yes** | Next.js最新の推奨ルーティング機能です |
| **Would you like to customize the default import alias?** | **No** | 通常はデフォルトの `@/*` で十分です |

---

## 3. 開発サーバーの起動

作成したプロジェクトディレクトリに移動し、開発用ローカルサーバーを起動します。

```bash
cd my-app
npm run dev

```

起動後、ブラウザで [http://localhost:3000](https://www.google.com/search?q=http://localhost:3000) にアクセスし、Next.jsのウェルカムページが表示されれば成功です。

---

## 4. ディレクトリ構成の基本

作成されたプロジェクトの主な構成は以下の通りです。

* **`src/app/`**: ルーティングやページ（`page.tsx`）、レイアウト（`layout.tsx`）を記述するメインディレクトリ。
* **`public/`**: 画像やフォントなどの静的ファイルを配置します。
* **`next.config.mjs`**: Next.jsの高度な設定を行うファイル。
* **`tailwind.config.ts`**: Tailwind CSSのデザインカスタマイズ用ファイル。

---

## 5. よく使うコマンド

開発中に頻繁に使用するコマンドです。

* `npm run dev`: 開発サーバーの起動（ホットリロード対応）
* `npm run build`: 本番環境用のビルド生成
* `npm run start`: ビルド済みファイルの実行
* `npm run lint`: 静的解析の実行

---

> **Note:**
> VS Codeを使用している場合は、拡張機能の **"ESLint"** と **"Tailwind CSS IntelliSense"** をインストールしておくと、開発効率が劇的に向上します。

---