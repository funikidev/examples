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
| [leo.funiki](leo.funiki) | Leo — cold, loyal companion | Japanese | 8 | companion, drama |
| [vera.funiki](vera.funiki) | Vera — dry, precise colleague | English | 12 | mentor, professional |
| [rin.funiki](rin.funiki) | Rin — quiet, poetic stranger | Japanese | 6 | mysterious, poetic |
| [max.funiki](max.funiki) | Max — founder energy | English | — | mentor, startup |

## Add your own

PRs welcome. One `.funiki` file per character. Keep it under 10KB.

Format: [spec/v1.0.md](https://github.com/funikidev/funiki/blob/main/spec/v1.0.md)
