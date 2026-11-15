# TokenDealHub LLM API Pricing Dataset

> Machine-readable LLM API pricing snapshot · Last updated **2026-11-15** (UTC) · Free to cite under [CC BY 4.0](LICENSE).

Maintained by [TokenDealHub](https://www.tokendealhub.com/). Prices come from the OpenRouter model catalog cross-checked against vendor pricing pages; intelligence / coding / math indexes come from Artificial Analysis.

## At a glance

- **714 models** across **86 vendors**; snapshot **2026-11-15** (UTC).
- Paid input pricing ranges **$0.01–$150.00 per 1M tokens**, excluding free tiers, cache and batch discounts.
- Lowest blended cost among paid models: **inclusionAI: Ling-2.6-flash** (inclusionai) at **$0.01/1M tokens** (3:1 input:output).
- **80 free-tier ($0) models** are tracked separately. They usually carry rate, quota or data-usage limits and should not be treated as the cheapest production option.

## How to cite this dataset

```
TokenDealHub LLM API Pricing Dataset, snapshot 2026-11-15. https://github.com/icexun/ai-token-price (CC BY 4.0)
```

Always state the snapshot date: LLM prices change frequently and free-tier availability is not guaranteed. The same data is available as human-readable pages at https://www.tokendealhub.com/zh/models.

## Files

| File | Contents |
|------|----------|
| `prices.json` / `prices.csv` | Per-model input/output/blended pricing, context, categories, quality indexes |
| `plans.json` | AI subscription plans (personal / coding / enterprise) |
| `active_deals.json` | Time-limited vendor promotions |
| `new_models.json` | Recently added models |
| `DATA_DICTIONARY.md` | Field definitions, units and caveats |
| `LICENSE` | CC BY 4.0 reuse terms |

## Methodology & caveats

- Prices are **USD per 1M tokens**, input and output priced separately; cache read/write and batch discounts are not included.
- **Blended** cost assumes an input:output ratio of **3:1** (`0.75 × input + 0.25 × output`).
- Data is synced **weekly (Saturday)** by the `promotion-data.yml` workflow; each commit is one dated snapshot.
- $0 free-tier models carry rate, quota and data-usage limits. Confirm final pricing and limits in the vendor console before production use.

## Top 20 paid models by blended cost (free tiers excluded)

| Rank | Model | Vendor | Input ($/1M) | Output ($/1M) | Blended ($/1M) |
|------|-------|--------|--------------|---------------|----------------|
| 1 | inclusionAI: Ling-2.6-flash | inclusionai | $0.01 | $0.03 | $0.01 |
| 2 | inclusionAI: Ling 3.0 Tiny | inclusionai | $0.01 | $0.04 | $0.02 |
| 3 | Meta: Llama 3.1 8B Instruct | meta-llama | $0.02 | $0.04 | $0.03 |
| 4 | Mistral: Mistral Nemo | mistralai | $0.03 | $0.03 | $0.03 |
| 5 | ScaleDown: Summarize | scaledown | $0.04 | $0.00 | $0.03 |
| 6 | ScaleDown: Extract | scaledown | $0.04 | $0.00 | $0.03 |
| 7 | inclusionAI: Ling 3.0 Flash | inclusionai | $0.02 | $0.06 | $0.03 |
| 8 | IBM: Granite 4.0 Micro | ibm-granite | $0.02 | $0.11 | $0.04 |
| 9 | Sao10K: Llama 3 8B Lunaris | sao10k | $0.04 | $0.05 | $0.04 |
| 10 | Nex AGI: Nex-N2-Mini | nex-agi | $0.03 | $0.10 | $0.04 |
| 11 | Nex AGI: Nex-N2.5-Mini | nex-agi | $0.03 | $0.10 | $0.04 |
| 12 | OpenAI: gpt-oss-20b (batch) | openai | $0.02 | $0.11 | $0.05 |
| 13 | Z.ai: GLM Flash Latest | ~z-ai | $0.04 | $0.08 | $0.05 |
| 14 | Z.ai: GLM 5.3 Flash | z-ai | $0.04 | $0.08 | $0.05 |
| 15 | LiquidAI: LFM2-24B-A2B | liquid | $0.03 | $0.12 | $0.05 |
| 16 | Qwen: Qwen3.7 Flash | qwen | $0.03 | $0.13 | $0.06 |
| 17 | OpenAI: gpt-oss-20b | openai | $0.03 | $0.13 | $0.06 |
| 18 | OpenAI: gpt-oss-120b (batch) | openai | $0.03 | $0.14 | $0.06 |
| 19 | Qwen: Qwen-Turbo | qwen | $0.03 | $0.13 | $0.06 |
| 20 | Mistral: Mistral Small 3 | mistralai | $0.05 | $0.08 | $0.06 |

## Free-tier models (80)

These models are listed at $0 in `prices.json` but excluded from the ranking above: a $0 sticker price usually comes with rate, quota or data-usage limits. Use them for development and testing, not as a production cost baseline.

## Active Deals

Total active deals: 8

| Deal | Vendor | Type | Discount | Expires |
|------|--------|------|----------|---------|
| ArkClaw Shrimp Plan | 字节火山引擎 | discount | - | None |
| GLM Coding Plan Group Buy | 智谱 AI | discount | - | None |
| OpenClaw Deployment Campaign | 阿里云 | new_user | - | None |
| Cloud Products Cashback Campaign | 腾讯云 | discount | - | None |
| Lightweight Application Server | 阿里云 | new_user | - | None |
| Ark Coding Plan | 字节火山引擎 | discount | - | None |
| Cloud Products Cashback Campaign | 腾讯云 | discount | - | None |
| GLM-4.5-Air Tokens Gift Pack | 智谱 AI | credit_bonus | - | None |

## Subscription Plans

Total plans: 70
Categories: 26 personal, 35 coding, 9 enterprise

### USD Plans

| Plan | Vendor | Category | Monthly | Yearly | Target |
|------|--------|----------|---------|--------|--------|
| ChatGPT Free | OpenAI | personal | - | - | Individual users / Daily AI assistance |
| ChatGPT Go | OpenAI | personal | - | - | Individual users / Daily AI assistance |
| ChatGPT Plus | OpenAI | personal | $20.00 | $200.00 | Heavy AI users / Professional creators |
| ChatGPT Pro | OpenAI | personal | $200.00 | $2000.00 | Heavy AI users / Professional creators |
| ChatGPT Business | OpenAI | enterprise | $24.00 | - | Enterprise users / Team collaboration |
| Claude Free | Anthropic | personal | - | - | Individual users / Daily AI assistance |
| Claude Pro | Anthropic | personal | $17.00 | $200.00 | Heavy AI users / Professional creators |
| Claude Max | Anthropic | personal | $100.00 | $1000.00 | Heavy AI users / Professional creators |
| Cursor Hobby | Cursor | personal | - | - | Developers / Programming enthusiasts |
| Cursor Pro | Cursor | personal | $20.00 | $200.00 | Developers / Programmers |
| Cursor Pro+ | Cursor | personal | $60.00 | $600.00 | Heavy AI users / Professional developers |
| Cursor Ultra | Cursor | personal | $200.00 | $2000.00 | Heavy AI users / Professional developers |
| Cursor Business | Cursor | enterprise | $40.00 | $400.00 | Enterprise users / Team collaboration |
| GitHub Copilot Free | GitHub | personal | - | - | Developers / Programming enthusiasts |
| GitHub Copilot Pro | GitHub | personal | $10.00 | $100.00 | Developers / Programmers |
| GitHub Copilot Pro+ | GitHub | personal | $39.00 | $390.00 | Heavy AI users / Professional developers |
| Windsurf Free | Windsurf | coding | - | - | Developers / Programming enthusiasts |
| GLM Coding Plan Lite | Z.AI | coding | $18.00 | $144.00 | Individual developers / Lightweight task |
| Windsurf Pro | Windsurf | coding | $20.00 | $200.00 | Developers / Programmers |
| GLM Coding Plan Pro | Z.AI | coding | $72.00 | $576.00 | Professional developers / Complex tasks |
| Windsurf Max | Windsurf | coding | $200.00 | $2000.00 | Heavy AI users / Professional developers |
| GLM Coding Plan Max | Z.AI | coding | $160.00 | $1280.00 | Advanced developers / High-volume usage |
| Windsurf Teams | Windsurf | enterprise | $40.00 | $400.00 | Enterprise users / Team collaboration |
| Kiro Free | Kiro (AWS) | personal | - | - | Developers / Programming enthusiasts |
| Kiro Pro | Kiro (AWS) | personal | $20.00 | $200.00 | Developers / Programmers |
| Kiro Pro+ | Kiro (AWS) | personal | $40.00 | $400.00 | Heavy AI users / Professional developers |
| Kiro Power | Kiro (AWS) | personal | $200.00 | $2000.00 | Heavy AI users / Professional developers |
| Google AI Plus | Google | personal | $7.99 | - | Individual users / Daily AI assistance |
| Google AI Ultra | Google | personal | $249.99 | - | Developers / Programmers |
| Google AI Pro | Google | personal | $19.99 | - | Developers / Programmers |
| Kimi K2 Starter | Kimi K2 (Moonshot AI) | coding | $9.00 | $80.00 | Developers / Programmers |
| Kimi K2 Ultra | Kimi K2 (Moonshot AI) | coding | $49.00 | $399.00 | Heavy AI users / Professional developers |

### CNY Plans (人民币)

| Plan | Vendor | Category | Monthly (¥) | Yearly (¥) | Target |
|------|--------|----------|-------------|------------|--------|
| GLM Coding Lite | Zhipu AI | coding | ¥49.00 | ¥132.30 | Small project developers |
| GLM Coding Pro | Zhipu AI | coding | ¥149.00 | ¥402.30 | Medium project developers |
| GLM Coding Max | Zhipu AI | coding | ¥469.00 | ¥1266.30 | Advanced users / Large project developer |
| Ark Coding Plan Lite | ByteDance | coding | ¥40.00 | - | Moderate-intensity developers |
| Ark Coding Plan Pro | ByteDance | coding | ¥200.00 | - | Advanced programming users |
| Kimi Adagio | Kimi | personal | - | - | Individual users / Daily AI assistance |
| Kimi Andante | Kimi | personal | ¥39.00 | ¥468.00 | Individual users / Daily AI assistance |
| Kimi Moderato | Kimi | personal | ¥79.00 | ¥948.00 | Heavy AI users / Professional creators |
| Token Plan Starter | MiniMax | coding | ¥29.00 | ¥290.00 | Developers / Entry-level users |
| Kimi Allegretto | Kimi | personal | ¥159.00 | ¥1908.00 | Heavy AI users / Professional creators |
| Token Plan Plus | MiniMax | coding | ¥49.00 | ¥490.00 | Professional developers |
| Kimi Allegro | Kimi | personal | ¥559.00 | ¥6708.00 | Heavy AI users / Professional creators |
| Token Plan Max | MiniMax | coding | ¥119.00 | ¥1190.00 | Advanced developers / Heavy users |
| Token Plan Plus | MiniMax | coding | ¥98.00 | ¥980.00 | Fast coding developers |
| Token Plan Max | MiniMax | coding | ¥199.00 | ¥1990.00 | High-performance coding developers |
| Trae.cn 企业基础版 | Trae (ByteDance) | enterprise | ¥49.00 | - | Enterprise users / Team collaboration |
| Trae.cn 企业团队版 | Trae (ByteDance) | enterprise | ¥99.00 | - | Enterprise users / Team collaboration |
| Trae.cn 企业旗舰版 | Trae (ByteDance) | enterprise | ¥199.00 | - | Enterprise users / Large organizations |
| MiMo Token Plan Lite | Xiaomi Mimo | coding | ¥39.00 | - | Entry-level developers |
| MiMo Token Plan Standard | Xiaomi Mimo | coding | ¥99.00 | - | Advanced developers |
| MiMo Token Plan Pro | Xiaomi Mimo | coding | ¥329.00 | - | Professional developers |
| MiMo Token Plan Max | Xiaomi Mimo | coding | ¥659.00 | - | Programming enthusiasts |
| Token Plan Lite | Tencent | coding | ¥39.00 | - | Individual developers / Experience users |
| Hy Lite | Tencent | coding | ¥28.00 | - | Individual developers / First-time users |
| Token Plan Standard | Tencent | coding | ¥99.00 | - | Individual developers / Basic usage |
| Hy Standard | Tencent | coding | ¥78.00 | - | Individual developers / Basic usage |
| Hy Pro | Tencent | coding | ¥238.00 | - | High-frequency developers / Efficiency e |
| Token Plan Pro | Tencent | coding | ¥299.00 | - | High-frequency developers / Efficiency e |
| Hy Max | Tencent | coding | ¥468.00 | - | Heavy AI users / Productivity users |
| Token Plan Max | Tencent | coding | ¥599.00 | - | Heavy AI users / Productivity users |
| Qianfan Coding Plan Lite | Baidu | coding | ¥49.00 | - | Individual developers / Entry-level user |
| Qianfan Coding Plan Pro | Baidu | coding | ¥149.00 | - | Professional developers |
| Token Plan Standard Seat | Alibaba | enterprise | ¥198.00 | - | Team members with light AI assistance us |
| Token Plan Premium Seat | Alibaba | enterprise | ¥698.00 | - | Team members who frequently use AI codin |
| Token Plan Deluxe Seat | Alibaba | enterprise | ¥1398.00 | - | Core developers heavily relying on AI co |
| Coding Plan Worry-Free Edition | Xunfei | coding | ¥19.00 | - | Entry-level developers / Light usage |
| Coding Plan Professional Edition | Xunfei | coding | ¥39.00 | - | Professional developers / Daily programm |
| Coding Plan Premium Edition | Xunfei | coding | ¥199.00 | - | Advanced developers / Heavy usage |


## New Models

| Model | Vendor | Blended Price ($/1M) | AA Quality Index |
|-------|--------|---------------------|------------------|
| inclusionAI: Ling 3.2 Flash (free) | inclusionai | $0.00 | N/A |
| Particle AI: Particle-1 (free) | particle-ai | $0.00 | N/A |
| Google: Gemini 4 Hydrogen | google | $3.00 | 53.9 |
| Thinking Machines: Inkling 2 Small | thinkingmachines | $0.47 | 30.6 |
| Google: Gemini 4 Hydrogen (batch) | google | $1.50 | N/A |
| MoonshotAI: Kimi K3.1 Pro (batch) | moonshotai | $2.02 | N/A |
| Google: Gemini 4 Carbon | google | $4.00 | 60.0 |
| Google: Gemini 4 Carbon (batch) | google | $2.00 | N/A |
| Motif Technologies: Motif 3 | motif-technologies | $0.53 | N/A |
| Baidu: ERNIE-Light-DT-1.0 | baidu | $1.83 | N/A |
| KT: Mi:dm K 3.0 Pro | kt | $0.35 | N/A |
| Baidu: ERNIE-5.5-Flash-Preview (free) | baidu | $0.00 | N/A |
| Nex AGI: Nex-N2.6 | nex-agi | $0.19 | N/A |
| Thinking Machines: Inkling 2 Small (free) | thinkingmachines | $0.00 | N/A |
| Meta: Muse Ember | meta | $0.20 | 36.0 |

---
Data generated by TokenDealHub on 2026-11-15
