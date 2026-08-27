# 東京七十二候 / Tokyo 72 Microseasons

> **二十四節気はそのまま残す。七十二候を、いまの東京からつくり直す。**

**東京七十二候**は、現代の東京で実際に出会える植物、鳥、虫、空、香り、音などをもとに、七十二候を再構成するオープンプロジェクトです。

太陽の運行によって決まる二十四節気を骨格として残し、その間を約5日ごとに刻む七十二候を、現代の生物季節・都市環境に合わせて再編集します。

This project proposes a contemporary set of **72 microseasons for Tokyo**, based on observable seasonal phenomena in today's city.

## Current version

**v0.4 — current baseline of 72 phenomena**

現象の選定は一旦確定とし、今後は各候の説明、根拠、観察条件、地域差、年変動などを整備していきます。

- Source of truth: [`data/tokyo_72kou.csv`](data/tokyo_72kou.csv)
- JSON: [`data/tokyo_72kou.json`](data/tokyo_72kou.json)
- Schema: [`data/schema.json`](data/schema.json)
- Evidence registry: [`sources/source_registry.csv`](sources/source_registry.csv)
- Methodology: [`docs/methodology.md`](docs/methodology.md)
- Source policy: [`docs/sources.md`](docs/sources.md)
- Mini app: [`app/index.html`](app/index.html)
- Working spreadsheet: https://docs.google.com/spreadsheets/d/1-pfuBzQFIka5AtnXefup-PPtC_P2_cmz1i1W8nQ962I/edit

## Web demo

The repository is GitHub Pages-ready. `index.html` redirects to the self-contained viewer in `app/`, and `.nojekyll` is included.

Once GitHub Pages is enabled for the `main` branch / repository root, the expected URL is:

`https://rhodanus2179.github.io/tokyo-72kou/`

## Design principles

1. **原則1種・1現象につき1候**
2. **開始を優先し、必要に応じて最盛期を採用**
3. **東京での観察可能性を重視**
4. **植物・鳥・昆虫・両生類・気象・天文・農景観・香り・音を織り交ぜる**
5. **夏至・秋分など二十四節気そのものとは原則重複させない**
6. **固定5日間は代表区間であり、実際の季節は年・場所・気象で動く**

## What this is — and isn't

東京七十二候は、古典七十二候の歴史的復元ではありません。また、生物季節観測の標準手法そのものでもありません。

これは、**現代の東京で人が季節の変化に気づくための、観察可能性を重視した編集的な暦**です。

将来的には、固定された暦と、その年・その場所で実際に起きている生物季節を重ねて扱うことを想定しています。

## Repository structure

```text
.
├── README.md
├── LICENSE
├── LICENSE-DATA
├── CONTRIBUTING.md
├── CHANGELOG.md
├── CITATION.cff
├── index.html
├── .nojekyll
├── data/
│   ├── tokyo_72kou.csv
│   ├── tokyo_72kou.json
│   └── schema.json
├── docs/
│   ├── methodology.md
│   ├── naming-policy.md
│   └── sources.md
├── sources/
│   └── source_registry.csv
└── app/
    └── index.html
```

## Data fields

| Field | Meaning |
|---|---|
| `id` | 1–72 の通し番号 |
| `month` | 月 |
| `start_day` / `end_day` | 暦上の代表区間 |
| `name` | 候名 |
| `reading` | よみ |
| `confidence` | 現時点の評価 |
| `category` | 生物・現象カテゴリ |
| `phase` | 開始／最盛／開始・最盛 |

## Evidence

候の時期や観察可能性を支える資料は `sources/source_registry.csv` に登録します。個別観察日、平年値、一般的な花期・飛来期は区別して記録し、単一資料だけで固定的な生物学的発生日を主張しません。

レジストリは継続整備中です。v0.4 の72現象が現在の基準版であることと、72候すべての根拠整理が完了していることは別です。

## Licensing

- **Source code**: MIT License
- **Dataset and original editorial content**: CC BY 4.0

第三者資料そのものは再配布せず、出典情報と判断根拠を整理していきます。各出典の権利はそれぞれの権利者に帰属します。

## Related project

東京七十二候は、東京都オープンデータハッカソン向けに開発した季節の自然推薦サービス「おりにつけ」の検討から派生しましたが、本リポジトリは独立したオープンプロジェクトとして運用します。

## Status

The project is in active editorial development. The 72 phenomena in v0.4 are treated as the current baseline; wording, evidence, metadata, and implementation details may continue to improve.
