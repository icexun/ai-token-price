# Data Dictionary · TokenDealHub LLM API Pricing Dataset

Snapshot cadence: weekly (Saturday, `promotion-data.yml`). Every commit is one dated snapshot.
License: [CC BY 4.0](LICENSE). Always cite the snapshot date.

## Snapshot fields

Every JSON file has `date` (`YYYY-MM-DD`, UTC) and `updated_at` (ISO 8601 UTC) at the top level, except `prices.json` / `prices.csv`, which are a flat array / table of records with a per-record `updated_at` (JSON only). Use those timestamps, not the git commit date, when stating data freshness.

## `prices.json` / `prices.csv`

One record per model with a valid price. Records with negative prices (sentinel dirty data) or with both input and output prices missing are excluded.

| Field | Type | Meaning |
|---|---|---|
| `model_name` | string | Human-readable model name |
| `model_id` | string | OpenRouter slug, e.g. `anthropic/claude-opus-4.7-fast` — the stable join key |
| `vendor` | string | Vendor / lab display name |
| `price_input` | number \| null | USD per 1M **input** tokens |
| `price_output` | number \| null | USD per 1M **output** tokens |
| `price_blended` | number \| null | Estimated cost per 1M tokens at an input:output ratio of **3:1** (`0.75 × input + 0.25 × output`), unless the upstream already supplies a blended value |
| `aa_quality_index` | number \| null | Artificial Analysis quality index; `null` when the model has not been benchmarked |
| `categories` | string[] | Task tags, e.g. `general`, `coding`, `text`, `agent`, `image-gen` |
| `updated_at` | string \| null | Last time **this model record** was synced (ISO 8601 UTC). **Present in `prices.json` only; `prices.csv` omits this column.** |

`categories` in `prices.csv` is a semicolon-separated string (`coding;general`), not a JSON array.

## `plans.json`

`plans[]`: `plan_name`, `vendor`, `vendor_id`, `category` (`personal` / `coding` / `enterprise`), `price_monthly`, `price_yearly`, `currency` (`USD` / `CNY`), `included_models[]`, `usage_quota{}`, `features[]`, `target_audience`, `affiliate_url`, `sort_order`. Top level also has `category_counts{}`.

Prices are **per month / per year in the stated currency**, not per token. `null` means the vendor has not published a price; `-` in the README table is the rendered form of `null`.

## `active_deals.json`

`deals[]`: `title`, `title_zh`, `vendor`, `vendor_id`, `type` (`discount` / `new_user` / `credit_bonus` / …), `description`, `discount_pct`, `coupon_code`, `model`, `affiliate_url`, `expires_at`, `is_featured`. Promotions are time-limited; always check `expires_at` before citing.

## `new_models.json`

`models[]`: `model_name`, `model_id`, `vendor`, `price{input,output,blended}`, `aa_quality_index`, `aa_intelligence_index`, `categories[]`, `context_length`, `published_at`. Note the nested `price` object (unlike the flat `prices.json`).

## Units and caveats

1. **All token prices are USD per 1M tokens.** Input and output are priced separately; cache read/write discounts, batch discounts and enterprise contracts are **not** included.
2. **Blended cost is an estimate**, not a billed amount: it assumes a 3:1 input:output ratio. Real bills depend on prompt length, cache hits, retries and failure rate.
3. **$0 free-tier models are not a production cost baseline.** They usually carry rate, quota and data-usage limits. The dataset README ranks paid models only and counts free tiers separately.
4. Benchmark indexes (`aa_*`) come from Artificial Analysis and may be `null` or lag behind price updates.
5. Prices are aggregated from OpenRouter and vendor public pricing pages. Always confirm the final quote in the vendor console before purchasing.

## Suggested citation

```
TokenDealHub LLM API Pricing Dataset, snapshot YYYY-MM-DD.
https://github.com/icexun/ai-token-price (CC BY 4.0)
```
