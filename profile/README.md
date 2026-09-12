# genai-*-onpre — ガバメントAI 源内 OSS のオンプレ派生
### docker compose up で動く日本語ローカルAI基盤（非公式）
### チャット/文書RAG/法令RAG/画像生成/文字起こし

デジタル庁がOSS公開したガバメントAI「源内」を、クラウドなしの単一ホストで動かすための非公式の派生実装です。
開発者 1 人が `docker compose up` で立ち上げて実験できることを目指しています。

**まずここから → [genai-deploy-onpre](https://github.com/sanpoyoshi-commons/genai-deploy-onpre)**

| リポジトリ | 役割 |
|---|---|
| [genai-deploy-onpre](https://github.com/sanpoyoshi-commons/genai-deploy-onpre) | 配布物（docker-compose 一式）。法令RAG 用データも Releases で配布 |
| [genai-ai-api-onpre](https://github.com/sanpoyoshi-commons/genai-ai-api-onpre) | AI アプリ API。LLM 抽象化・文書RAG・法令RAG・画像・文字起こし |
| [genai-web-onpre](https://github.com/sanpoyoshi-commons/genai-web-onpre) | Web フロントエンド。チャットUI・RAG・データ分析UI、OIDC (PKCE) |
| [genai-workflow-runner](https://github.com/sanpoyoshi-commons/genai-workflow-runner) | TOML で多段 AI ワークフローを定義・実行する汎用ランナー（完全オリジナル） |

上流は [digital-go-jp/genai-web](https://github.com/digital-go-jp/genai-web) および
[genai-ai-api](https://github.com/digital-go-jp/genai-ai-api) です。本組織のリポジトリは
独立・非公式の派生であり、デジタル庁およびその公式プロジェクトとは関係がなく、
提携・推奨・認証・保証を受けたものではありません。開発・実験用の無保証ソフトウェアで、
本番業務や機微データの取扱いは想定していません。

### はじめかた

1. [genai-deploy-onpre](https://github.com/sanpoyoshi-commons/genai-deploy-onpre) を clone
2. README の初期設定(証明書・secrets 生成・web ビルド)を実行
3. `docker compose up -d`

### 免責
コードのライセンス許諾は、公式ロゴ等のブランド要素の使用許諾を含みません。
本プロジェクトはデジタル庁およびその公式プロジェクトとは一切関係がなく、提携・推奨・公認を受けたものではありません。
開発・実験用の無保証ソフトウェアであり、本番業務や実際の個人情報・機微なデータの取り扱いは想定していません。
詳細は各リポジトリの DISCLAIMER.md を参照してください。

### 開発者

坂本梨風 (Rifu Sakamoto) — [note](https://note.com/rifu_sakamoto)
