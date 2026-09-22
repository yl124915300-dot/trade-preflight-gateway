# Trade Preflight Gateway

A **cross-border trade** **MCP server** for pre-transaction checks on China to US and China to EU physical goods shipments.

## Remote endpoint

- Streamable HTTP: https://china-sourcing-router.naijunyu.chatgpt.site/api/trade-preflight-mcp
- Official MCP Registry: [io.github.yl124915300-dot/trade-preflight@0.1.0](https://registry.modelcontextprotocol.io/v0/servers/io.github.yl124915300-dot%2Ftrade-preflight/versions/0.1.0)

## What it does

Trade Preflight Gateway organizes a dated customs preflight before a transaction. It helps structure landed cost, tariff, de minimis, and import-requirement questions for a narrow China to US/EU corridor.

Tools:

- trade_preflight - run a corridor preflight and return an evidence-aware status.
- check_trade_requirements - check required trade and import fields for the selected corridor.
- normalize_supplier_quote - normalize supplier quote inputs for comparable landed-cost review.
- compare_preflight_quotes - compare preflight quote records while preserving uncertainty.

## Scope

- China to United States and China to European Union corridors.
- Low-regulation physical goods and pre-transaction planning.
- Landed-cost structure, customs preflight, tariff and de minimis questions, and missing-data detection.

## Safety and limits

Estimates only. Uncertain HS classification, tariff, PGA, antidumping/countervailing-duty, or other regulated cases return NEEDS_MORE_DATA or MANUAL_REVIEW rather than a definitive result. This server is not customs, tax, import, export, or legal advice. Confirm requirements with the relevant authorities or a qualified professional before shipping or paying.

This repository contains public documentation and metadata only. It does not contain private business code, credentials, D1 data, or internal paths.

## Connection

Add the remote endpoint above to an MCP-compatible client using Streamable HTTP. The endpoint exposes the four tools listed here and supports no paid listing or hosted upsell.
