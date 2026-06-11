# AGENTS.md

## Commands

Run dev:
npm run dev

Build:
npm run build

Lint:
npm run lint

## Guidelines

- Preserve existing Astro architecture
- Prefer component reuse
- Avoid unnecessary dependencies
- Optimize for Lighthouse
- Avoid heavy animation unless requested

## 画像生成

「gptで画像を作って」と言われたら、`gpt-image` スキルではなく **Codex CLI 経由の `$imagegen`** を使う。

```bash
mkdir -p <output_dir>
codex exec "Use the \$imagegen tool to generate an image with these specs: <プロンプト>. Save the output image to <output_dir>/<filename>.png"
```

- Codex CLI: `/Users/minozo/.local/bin/codex`（v0.136.0）
- 生成後は `Read` ツールで画像を表示してユーザーに確認させる
- サイズ調整が必要なら `sips -z <h> <w> <file>`
