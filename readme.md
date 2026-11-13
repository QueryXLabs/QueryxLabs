# QueryXLabs

we build ai infra that shows its receipts

fuck vibes, ship proof

## what we ship

| thing | what it does |
|---|---|
| **QuantAI** | agent platform, you chat with agents, creators build them in Studio, everybody gets paid through the Marketplace, agents stop and ask a human before any external write, still cooking and not prod ready, we wrote that in our own readme |
| **QueryX** | ai search engine you self host, hits the live web, reads the full pages, puts a source on every claim, no ads and no seo garbage |
| **QueryxBot** | our own crawler and index, real user agent, respects the rules of the sites it visits, answers nothing without evidence |
| **AWP** | agentic web protocol, sites tell agents what is where so agents quit scraping html like raccoons in a dumpster |
| **AgentAd** | click an ad and talk to a branded assistant that only says what the advertiser approved, if it cant back a claim it shuts up |
| **Cabby** | one prompt in, verified editable app out |

## the modules

lego for agents, python and js flavors

| module | job |
|---|---|
| Security | kms, vault, policy, tokens, threat scoring, soc2 evidence packs |
| Guardrails | catches the attacks, enforces the budgets, keeps agents from going off the rails |
| Passport | signed identity for agents, replay a passport and it throws, revoke one and it dies on the next check |
| LLM | one interface for every model provider |
| RAG | retrieval for your docs |
| Tool | tool providers behind one door |
| Skill | agents pick up new behaviors from yaml or SKILL md files |
| Sandbox | sandboxed execution for agent code |

## how a request lives

```
request
  Security      who are you and do we like your ip
  Guardrails    are you trying to jailbreak us
  Passport      what is this agent allowed to touch
  LLM RAG Tool Skill Sandbox      go do the work
```

## house rules

- no evidence no answer
- we never fake our crawler identity
- noindex means noindex
- private networks stay private
- if the model cant back it up it says nothing

## receipts

in our recorded benchmark run with a Gemini Flash Lite model, agents on plain html finished 0 of 3 real site tasks and agents on AWP finished 3 of 3

tiny sample, we wrote it down anyway, the full report lives in the AWP repo

AWP docs: https://awp-docs.pages.dev/

## where is the code

30 repos, most of them private for now

you get the readme and the attitude
