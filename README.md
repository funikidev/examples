# funiki examples

Ready-to-use persona packs. Download any `.funiki` file and attach it to your AI chat.

## How to use

```bash
# Option 1: render to prompt and copy to clipboard
npx funiki render leo.funiki | pbcopy
# Then paste into ChatGPT, Claude, or any AI chat

# Option 2: use in code
import { load, render } from 'funiki'
const pack = load(fs.readFileSync('leo.funiki', 'utf-8'))
const systemPrompt = render(pack)
```

## Packs

| File | Character | Language | Turns | Tags |
|---|---|---|---|---|
| [leo.funiki.json](leo.funiki.json) | Leo — cold, loyal companion | Japanese | 8 | companion, drama |
| [vera.funiki.json](vera.funiki.json) | Vera — dry, precise colleague | English | 12 | mentor, professional |
| [rin.funiki.json](rin.funiki.json) | Rin — quiet, poetic stranger | Japanese | 6 | mysterious, poetic |
| [max.funiki.json](max.funiki.json) | Max — founder energy | English | — | mentor, startup |
| [leo-mask.funiki.json](leo-mask.funiki.json) | Leo (mask form) — reference for v1.1 `privacy: "mask"` | Japanese | 8 | reference, v1.1 |

## Privacy modes

`leo.funiki.json` and `leo-mask.funiki.json` are the same character — the second one wraps the sensitive fields into a base64 `payload` so casual readers can't peek. Both render identically once an SDK loads them. See [spec §17](https://github.com/funikidev/funiki/blob/main/spec/v1.1.md#17-privacy-modes-v11).

## Add your own

PRs welcome. One `.funiki.json` file per character. Keep it under 10KB.

Format: [spec/v1.1.md](https://github.com/funikidev/funiki/blob/main/spec/v1.1.md)
