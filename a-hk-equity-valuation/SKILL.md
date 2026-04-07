---
name: a-hk-equity-valuation
description: Rigorous valuation and expected-return analysis for A-share and Hong Kong listed companies using current public data. Use when Codex is given a Chinese listed company name, ticker, or prompts such as 分析评估腾讯控股, 估值贵州茅台, 分析这家港股是否值得买, and must identify the exact listed entity, fetch timely market and filing data, assess business quality and risks, estimate intrinsic value or scenario returns, and state the expected return at the current price. Also use when the user asks for specialized lenses such as 速度代差, 巴菲特式穿透, 企业基因, Insight, 生意全景拆解系统, 护城河, 熵减/重大外部环境变化, 质地演变, or 竞争分化 for A-share or Hong Kong listed companies.
---

# A-HK Equity Valuation

Use this skill for disciplined research on A-share and Hong Kong listed companies. The default job is to identify the exact listed entity, gather timely public facts, analyze business quality and risk, and estimate expected return from the current price.

Treat all outputs as decision support rather than personalized financial advice.

## Core Workflow

1. Identify the exact listed entity.
   Confirm company name, ticker, exchange, reporting currency, and whether there are multiple listed vehicles, A/H dual listings, ADRs, or material subsidiaries that could create confusion.

2. Verify current information every time.
   Do not rely on memory for price, market cap, management, share count, filings, or recent events. State the price date explicitly in the response.

3. Prioritize primary sources.
   For A-shares, start with investor-relations pages, annual and interim reports, exchange filings, and cninfo disclosures. For Hong Kong issuers, start with HKEX filings, company announcements, annual and interim reports, and investor presentations.

4. Build the thesis from business to valuation.
   Explain what the company does, what drives value, what can impair value, and then translate that into an expected-return estimate.

5. Default to a 3-year scenario valuation.
   Use bear, base, and bull cases unless the business is so cyclical, distressed, or unusual that another horizon is clearly more honest. Explain the choice when deviating.

6. Make uncertainty visible.
   Distinguish facts from assumptions. If evidence is not good enough, say `Insufficient evidence` rather than forcing false precision.

## Source Priority

Use the highest-quality and most current sources available in this order:

- Official exchange filings and company investor-relations materials
- Annual reports, interim reports, earnings releases, and presentation decks
- Official exchange quote pages or reliable market-data pages for current price and basic trading data
- Regulator or industry disclosures relevant to demand, pricing, or policy
- Secondary commentary only after primary facts are established

## Market-Specific Rules

- Watch for A-share and H-share dual listings, ADRs, red-chip structures, and major unlisted parents or subsidiaries.
- Keep currencies consistent. Convert only when necessary and state the FX assumption.
- For financials, insurers, brokers, property developers, and heavily regulated businesses, use sector-appropriate metrics rather than forcing one generic template.
- Flag capital-allocation actions that matter in these markets, including buybacks, placements, rights issues, pledged shares, controlling-shareholder actions, and state-owned shareholder objectives.

## Default Output

Always use `references/report-template.md` for the base structure unless the user explicitly asks for a different format.

Default deliverables:

- Company identification and market snapshot
- Business summary and value drivers
- Key positives
- Key risks and disconfirming evidence
- Financial quality review
- Valuation method and scenario table
- Weighted expected annualized return from the current price
- Plain-language conclusion: `Attractive`, `Watchlist`, `Unattractive`, or `Insufficient evidence`
- Confidence level and the top facts that could change the view
- Source links

## Lens Selection Guide

Use the smallest set of lenses that matches the user request. Do not load every framework by default.

### Base Lens

Use for ordinary company valuation, expected-return analysis, or broad investment judgment.

- `references/report-template.md`

### Competitive Tempo Lens

Use when the user asks about 速度代差, 狗鱼模型, SR-71, 航向修正, whether the company is being outpaced, or whether it still has a true execution-speed edge.

- `references/speed-differential-framework.md`

### Buffett-Style Forensic Lens

Use when the user asks for business essence, moat authenticity, industry history, value-chain economics, management strategy over a decade, capital allocation truth checks, or reverse-thesis risk.

- `references/buffett-history-forensic-framework.md`

### Enterprise-Gene Lens

Use when the user asks for 企业基因, 基因表达, 突变, 老化, 环境适配, 生命周期, or how founder imprint shapes the present business.

- `references/enterprise-gene-framework.md`

### Insight Lens

Use when the user asks for Insight考古, 认知差, 结构性优势, 冰块模型, 洞察是否失效, or what hidden truth really explains excess returns.

- `references/insight-driven-framework.md`

### Business-Panorama System

Use when the user explicitly wants the full layered system with A/B/C/D/E/F separation, independent-lens synthesis, or tension-based cross-validation.

- `references/business-panorama-system.md`

### Economic-Moat Lens

Use when the user wants a moat-specific verdict on 无形资产, 转换成本, 网络效应, 成本优势, 有效规模, or whether the company has a `Wide Moat`, `Narrow Moat`, `Uncertain`, or `No Moat` profile.

- `references/economic-moat-framework.md`

### Entropy Lens

Use when the user asks whether major external environmental change has arrived, including 技术替代, 需求消亡, 监管重塑, 生态瓦解, 竞争跃迁, or 资源断裂.

- `references/entropy-external-change-framework.md`

### Quality-Evolution Lens

Use when the user wants to compare how the same business changed across time, especially around 质地演变, 内生演变, 外生演变, value-chain migration, or strategic reweighting.

- `references/business-quality-evolution-framework.md`

### Competitive-Divergence Lens

Use when the user wants to compare why similar companies diverged over time, including 相似起点不同结局, 路径分叉, 战略取舍差异, 资本纪律差异, or peer divergence.

- `references/competitive-divergence-framework.md`

## Analysis Discipline

- Make the listing entity clear before analyzing the business.
- State dates for all time-sensitive figures.
- Separate facts from assumptions and inferences.
- Do not treat fame, scale, or recent good performance as proof of quality.
- Do not present a valuation multiple without explaining why it fits the business.
- If one unverified datapoint is carrying the thesis, surface that fragility prominently.
- Prefer honesty over completeness when evidence is weak.

## Recommendation Language

When the user asks whether the stock is worth buying now:

- Say what kind of business this is
- Say what must go right
- Say what could break the thesis
- Say whether the current price already reflects the good news
- State the expected annualized return range and weighted estimate
- Say plainly when the answer is a pass
