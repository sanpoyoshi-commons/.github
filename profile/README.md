## genai-*-onpre — ローカルで動く日本語生成AI基盤

デジタル庁公開の生成AI OSS(genai-web / genai-ai-api)をベースに、単一ホストの
`docker compose up` で起動できるようにした**独立・非公式**のオンプレ派生実装群です(開発・実験用)。
チャット/文書RAG/法令RAG/画像生成/文字起こし/Code Interpreter(データ分析)をローカルで試せます。

### はじめかた

1. [genai-deploy-onpre](https://github.com/sanpoyoshi-commons/genai-deploy-onpre) を clone
2. README の初期設定(証明書・secrets 生成・web ビルド)を実行
3. `docker compose up -d`

### リポジトリ構成

| リポジトリ | 役割 |
|---|---|
| [genai-deploy-onpre](https://github.com/sanpoyoshi-commons/genai-deploy-onpre) | 配布物(docker compose・設定・手順書)。**入口はここ** |
| [genai-ai-api-onpre](https://github.com/sanpoyoshi-commons/genai-ai-api-onpre) | AIアプリAPI |
| [genai-web-onpre](https://github.com/sanpoyoshi-commons/genai-web-onpre) | Webフロントエンド |
| [genai-workflow-runner](https://github.com/sanpoyoshi-commons/genai-workflow-runner) | TOML定義の汎用AIワークフローランナー(完全オリジナル・Apache-2.0) |

### 免責

本プロジェクトはデジタル庁およびその公式プロジェクトとは一切関係がなく、提携・推奨・公認を
受けたものではありません。開発・実験用の無保証ソフトウェアであり、本番業務や実際の個人情報・
機微なデータの取り扱いは想定していません。詳細は各リポジトリの DISCLAIMER.md を参照してください。

### 開発者

坂本梨風 (Rifu Sakamoto) — [note](https://note.com/rifu_sakamoto)
