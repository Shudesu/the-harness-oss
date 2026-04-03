# The Harness

**Open-source SNS automation for everyone.**

Replace Lステップ, Xステップ, and ManyChat — all free, self-hosted on Cloudflare.

**SNS自動化をOSSで、すべての人に。**

Lステップ・Xステップ・ManyChat、全部不要。無料・セルフホスト・Cloudflare完結。

---

## Channels

| Channel | Replaces | Repo | Status |
|---------|----------|------|--------|
| [LINE Harness](https://github.com/Shudesu/line-harness-oss) | Lステップ / Utage | `Shudesu/line-harness-oss` | Live |
| [X Harness](https://github.com/Shudesu/x-harness-oss) | Xステップ | `Shudesu/x-harness-oss` | Live |
| [IG Harness](https://github.com/Shudesu/instagram-harness-oss) | ManyChat / iステップ | `Shudesu/instagram-harness-oss` | Live |

> More channels coming — WhatsApp, Telegram, and beyond.
>
> WhatsApp、Telegram など今後追加予定。

---

## Architecture / アーキテクチャ

```
┌─────────────────────────────────────────────┐
│              The Harness                     │
│                                              │
│  ┌───────────┐ ┌──────────┐ ┌────────────┐  │
│  │   LINE    │ │    X     │ │     IG     │  │
│  │  Harness  │ │  Harness │ │   Harness  │  │
│  └─────┬─────┘ └────┬─────┘ └─────┬──────┘  │
│        │             │             │          │
│        └─────────────┼─────────────┘          │
│                      │                        │
│              ┌───────┴────────┐               │
│              │  Unified SDK   │               │
│              │  Unified MCP   │               │
│              └───────┬────────┘               │
│                      │                        │
│              ┌───────┴────────┐               │
│              │  Plugin System │               │
│              └───────┬────────┘               │
│                      │                        │
│              ┌───────┴────────┐               │
│              │  Marketplace   │               │
│              │  (Coming Soon) │               │
│              └────────────────┘               │
└─────────────────────────────────────────────┘

Infrastructure: Cloudflare Workers + D1 + R2
Cost: $0 (within free tier)
```

---

## Why The Harness? / なぜ The Harness？

### English

- **$0 infrastructure** — Runs on Cloudflare's free tier. No monthly SaaS fees.
- **Own your data** — Everything lives in your Cloudflare account. No vendor lock-in.
- **AI-native** — Built for Claude Code. Deploy with a single command, operate with natural language.
- **Plugin ecosystem** — Extend with community-built plugins, templates, and integrations.
- **Cross-channel** — Manage LINE, X, and Instagram from one system.

### 日本語

- **インフラ代 $0** — Cloudflare無料枠で完結。月額SaaS費用なし。
- **データは自分のもの** — 全データが自分のCloudflareアカウント内。ベンダーロックインなし。
- **AI前提設計** — Claude Code対応。ワンコマンドでデプロイ、自然言語で運用。
- **プラグイン経済圏** — コミュニティが作るプラグイン・テンプレ・連携で拡張。
- **クロスチャネル** — LINE・X・Instagramを一つのシステムで管理。

---

## Quick Start

Each channel can be deployed independently with a single command:

各チャネルはワンコマンドで独立デプロイできます：

```bash
# LINE
npx create-line-harness

# X
npx create-x-harness

# Instagram
npx create-instagram-harness
```

> Requires: Node.js 18+, Cloudflare account (free), Claude Code
>
> 必要なもの: Node.js 18+、Cloudflareアカウント（無料）、Claude Code

---

## Marketplace (Coming Soon)

The Harness Marketplace — where builders meet businesses.

Harnessマーケットプレイス — 作る人と使いたい人が出会う場所。

- **Templates** — Industry-specific automation packs / 業種別自動化パック
- **Plugins** — Community-built extensions / コミュニティ製プラグイン
- **Partners** — Certified implementation experts / 認定導入パートナー

> Interested in becoming a partner? Watch this repo.
>
> パートナーに興味がある方はこのリポジトリをWatchしてください。

---

## Roadmap

- [x] LINE Harness — Live
- [x] X Harness — Live
- [x] IG Harness — Live
- [ ] Unified contact identity (cross-channel)
- [ ] The Harness Marketplace
- [ ] WhatsApp Harness
- [ ] Telegram Harness
- [ ] Unified dashboard

---

## Community

- [GitHub Discussions](https://github.com/Shudesu/the-harness-oss/discussions) — Questions, ideas, and feedback
- [Issues](https://github.com/Shudesu/the-harness-oss/issues) — Bug reports and feature requests

---

## License

MIT — Use it however you want. Free forever.

MIT — 好きなように使ってください。永久無料。
