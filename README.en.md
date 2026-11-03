# launch-sources

[中文](README.md)

**130 public sources for new launches and tool directories.**

Curated by Fan Shifu ([@fanshifu](https://x.com/FanShifu)).

Prepared on 2026-11-03. 130 entries. This is a snapshot and is not updated automatically.

License: [MIT License](LICENSE).

## Files

| File | Content |
| --- | --- |
| `README.md` | Chinese version of this document |
| `README.en.md` | English version, this file |
| `sources.json` | JSON array of 130 objects, five fields each |
| `sources.csv` | The same table, UTF-8, no BOM |
| `LICENSE` | MIT License |

## What this is

I use these 130 public addresses to see what launched. There are 58 new-product launch platforms, 44 AI tool directories, 25 SaaS and general tool directories, and 3 community and content platforms. I screened more than 1,000 directory and launch sites and kept these 130, which can still be read in public.

This repository holds the list, this document, and the MIT license.

## Fields

| Field | Meaning |
| --- | --- |
| `name` | Site label, usually a domain |
| `url` | Public address to read |
| `category` | Category label for the Chinese edition |
| `category_en` | English category, one of the four names below |
| `method` | Fetch-method code |

`sources.json` is an array. Each object uses this key order: `name`, `url`, `category`, `category_en`, `method`. This page uses `category_en`.

```json
{
  "name": "betalist.com",
  "url": "https://feeds.feedburner.com/BetaList",
  "category_en": "New-product launch platforms",
  "method": "rss"
}
```

`sources.csv` uses the same columns and the same order. Rows are grouped by `category_en` in the order below, then by name, case-insensitive. A name is sometimes a different host from the address. The BetaList feed is on FeedBurner. The other mismatches are listed at the end.

## Categories

| Category | Count | What it covers |
| --- | ---: | --- |
| New-product launch platforms | 58 | New product launches, weekly drops, and launch lists |
| AI tool directories | 44 | AI tool directories and their latest listings |
| SaaS and general tool directories | 25 | SaaS, indie-developer tools, and general directories |
| Community and content platforms | 3 | Dev.to, Hacker News Show HN, and Product Hunt |

`category_en` is one of those four names, in that order. The catalog below uses the same names.

## Fetch methods

| Method | Count | Meaning |
| --- | ---: | --- |
| `sitemap` | 60 | Public sitemap. Addresses that were not in the previous copy are the new pages. |
| `html` | 37 | Public listing page. |
| `rss` | 18 | Public RSS or Atom feed. |
| `mcp` | 5 | Public MCP endpoint. The list includes no tool name, arguments, or credentials. |
| `html_cards` | 4 | Repeated cards on a listing page. |
| `json_api` | 3 | Public JSON. |
| `shopify_json` | 1 | Public Shopify products.json for a collection. |
| `hn_api` | 1 | Hacker News search on Algolia, limited to Show HN. |
| `ph_graphql` | 1 | Product Hunt. The published address is the public RSS feed, with no GraphQL query and no credential. |

Read an existing API or feed first, then a listing page, then diff a sitemap against the previous copy. `method` says which of those fits the address.

The `ph_graphql` row points at `https://www.producthunt.com/feed`.

Query strings already on these addresses are public filters: language, sort, page size, or a tag. Examples: `tag=showdev`, `per_page=30`, `limit=60`, `tags=show_hn`, `lg=en`, `sort=time_desc`.

## Use

Follow each site's robots.txt and terms, and leave a polite interval between requests. A row means the public page is in this watch list. Trademarks and terms stay with that site.

## Scope

The list contains public pages, public feeds, public sitemaps, or public APIs. It does not include access tokens, cookies, accounts, paid API configuration, internal paths, or private IP addresses.

## License

[MIT License](LICENSE). Copyright (c) 2026 Fan Shifu. You can copy, modify, and distribute this list if you keep the copyright notice and the permission notice. Trademarks stay with each site.

## Catalog

Same order as `sources.json` and `sources.csv`.

### New-product launch platforms (58)

| Name | URL | Category | Method |
| --- | --- | --- | --- |
| 1000.tools | https://1000.tools/sitemap.xml | New-product launch platforms | sitemap |
| altern.ai | https://altern.ai/recent | New-product launch platforms | html |
| auraplusplus.com | https://auraplusplus.com/launches | New-product launch platforms | html |
| betalist.com | https://feeds.feedburner.com/BetaList | New-product launch platforms | rss |
| buildvoyage.com | https://buildvoyage.com/sitemaps/pages.xml | New-product launch platforms | sitemap |
| businesshunt.co | https://businesshunt.co/sitemap.xml | New-product launch platforms | sitemap |
| curlship.com | https://curlship.com/sitemap.xml | New-product launch platforms | sitemap |
| devhunt.org | https://devhunt.org/upcoming | New-product launch platforms | html |
| fazier.com | https://fazier.com/ | New-product launch platforms | html |
| findly.tools | https://findly.tools/sitemap.xml | New-product launch platforms | sitemap |
| firsto.co | https://firsto.co/sitemap.xml | New-product launch platforms | sitemap |
| founder.best | https://www.founder.best/api/mcp | New-product launch platforms | mcp |
| foundrlist.com | https://www.foundrlist.com/feeds/products.xml | New-product launch platforms | rss |
| griv.io | https://griv.io/sitemap | New-product launch platforms | sitemap |
| huntifyai.com | https://huntifyai.com/tools?sort=time_desc | New-product launch platforms | html |
| huzzler.so | https://huzzler.so/sitemap.xml | New-product launch platforms | sitemap |
| ideakiln.com | https://ideakiln.com/ideas/today | New-product launch platforms | html |
| indiehub.best | https://indiehub.best/sitemap.xml | New-product launch platforms | sitemap |
| indiepa.ge | https://indiepa.ge/new | New-product launch platforms | html |
| indietool.io | https://www.indietool.io/sitemap.xml | New-product launch platforms | sitemap |
| launchboosts.com | https://launchboosts.com/ | New-product launch platforms | html_cards |
| launchbuff.com | https://launchbuff.com/sitemap.xml | New-product launch platforms | sitemap |
| launchigniter.com | https://launchigniter.com/sitemap.xml | New-product launch platforms | sitemap |
| launchvault.dev | https://www.launchvault.dev/trending | New-product launch platforms | html |
| microlaunch.net | https://microlaunch.net/sitemap-0.xml | New-product launch platforms | sitemap |
| nicklaunches.com | https://nicklaunches.com/ | New-product launch platforms | html |
| open-launch.com | https://open-launch.com/sitemap.xml | New-product launch platforms | sitemap |
| openhunts.com | https://openhunts.com/sitemap.xml | New-product launch platforms | sitemap |
| peerpush.net | https://peerpush.com/api/mcp | New-product launch platforms | mcp |
| pitchwall.co | https://pitchwall.co/rss | New-product launch platforms | rss |
| productfame.com | https://productfame.com/trending | New-product launch platforms | html |
| productwatch.io | https://productwatch.io/launches/day | New-product launch platforms | html |
| rankinpublic.xyz | https://rankinpublic.xyz/sitemap-0.xml | New-product launch platforms | sitemap |
| saascity.io | https://saascity.io/live | New-product launch platforms | html |
| saasfame.com | https://saasfame.com/sitemap.xml | New-product launch platforms | sitemap |
| saashunt.best | https://saashunt.best/sitemap/0.xml | New-product launch platforms | sitemap |
| scrolllaunch.com | https://www.scrolllaunch.com/api/mcp | New-product launch platforms | mcp |
| shinylaunch.com | https://shinylaunch.com/latest | New-product launch platforms | html |
| shipboost.io | https://shipboost.io/launches/weekly | New-product launch platforms | html |
| shipstry.com | https://shipstry.com/rss.xml | New-product launch platforms | rss |
| similarlabs.com | https://similarlabs.com/zh/launches | New-product launch platforms | html |
| smollaunch.com | https://smollaunch.com/api/v1/products | New-product launch platforms | json_api |
| startupbase.io | https://startupbase.io/launches | New-product launch platforms | html |
| startupfa.st | https://www.startupfa.st/trending | New-product launch platforms | html |
| startupstash.com | https://startupstash.com/page-sitemap.xml | New-product launch platforms | sitemap |
| submithunt.com | https://www.submithunt.com/sitemap.xml | New-product launch platforms | sitemap |
| sumodir.com | https://sumodir.com/sitemap.xml | New-product launch platforms | sitemap |
| tinyhunt.dev | https://tinyhunt.dev/sitemap/0.xml | New-product launch platforms | sitemap |
| tinylaunch.com | https://tinylaunch.com/sitemap.xml | New-product launch platforms | sitemap |
| tinylaunchpad.com | https://tinylaunchpad.com/sitemap.xml | New-product launch platforms | sitemap |
| tinystartups.com | https://www.tinystartups.com/today | New-product launch platforms | html |
| toolatlas.io | https://toolatlas.io/launches | New-product launch platforms | html |
| toolhunter.ai | https://toolhunter.ai/sitemap.xml | New-product launch platforms | sitemap |
| tools.launchllama.co | https://tools.launchllama.co/sitemap.xml | New-product launch platforms | sitemap |
| turbo0.com | https://turbo0.com/collection/new-this-month | New-product launch platforms | html |
| uneed.best | https://mcp.uneed.best/mcp | New-product launch platforms | mcp |
| vibecodinglist.com | https://vibecodinglist.com/sitemap.xml | New-product launch platforms | sitemap |
| whatlaunched.today | https://whatlaunched.today/feed.xml | New-product launch platforms | rss |

### AI tool directories (44)

| Name | URL | Category | Method |
| --- | --- | --- | --- |
| aiagentsdirectory.com | https://aiagentsdirectory.com/sitemap.xml | AI tool directories | sitemap |
| aibesttop.com | https://aibesttop.com/sitemap.xml | AI tool directories | sitemap |
| aidirectori.es | https://www.aidirectori.es/sitemaps/static.xml | AI tool directories | sitemap |
| aihubs.ai | https://aihubs.ai/sitemap.xml | AI tool directories | sitemap |
| aistage.net | https://aistage.net/tools/latest | AI tool directories | html |
| aitoolly.com | https://aitoolly.com/ai-news/rss.xml | AI tool directories | rss |
| aitoolnet.com | https://www.aitoolnet.com/new | AI tool directories | html_cards |
| aitools.inc | https://aitools.inc/sitemap.xml | AI tool directories | sitemap |
| aitoolsclub.com | https://aitoolsclub.com/rss/ | AI tool directories | rss |
| aitoolsdirectory.com | https://aitoolsdirectory.com/items.rss | AI tool directories | rss |
| aitooltrek.com | https://aitooltrek.com/sitemap.xml | AI tool directories | sitemap |
| aivalley.ai | https://aivalley.ai/feed/ | AI tool directories | rss |
| aiwith.me | https://aiwith.me/sitemap.xml | AI tool directories | sitemap |
| aixploria.com | https://www.aixploria.com/feed | AI tool directories | rss |
| bestofai.com | https://bestofai.com/new-tools | AI tool directories | html |
| codehype.ai | https://www.codehype.ai/v1/launches | AI tool directories | json_api |
| creati.ai | https://creati.ai/ai-tools/new/ | AI tool directories | html |
| dang.ai | https://dang.ai/new | AI tool directories | html |
| firstlook.tools | https://firstlook.tools/sitemap.xml | AI tool directories | sitemap |
| futurepedia.io | https://www.futurepedia.io/sitemap.xml | AI tool directories | sitemap |
| futuretools.io | https://futuretools.io/sitemaps/pages.xml | AI tool directories | sitemap |
| goodaitools.com | https://goodaitools.com/latest | AI tool directories | html |
| gptdemo.net | https://www.gptdemo.net/gpt/today?lg=en | AI tool directories | html |
| iuu.ai | https://iuu.ai/sitemap.xml | AI tool directories | sitemap |
| magicbox.tools | https://magicbox.tools/latest | AI tool directories | html |
| mossai.org | https://mossai.org/ | AI tool directories | html_cards |
| nxgntools.com | https://www.nxgntools.com/launching | AI tool directories | html |
| poweredbyai.app | https://poweredbyai.app/latest-tools | AI tool directories | html |
| rankyourai.com | https://rankyourai.com/rss.xml/ | AI tool directories | rss |
| saasaitools.com | https://saasaitools.com/feed/ | AI tool directories | rss |
| seektool.ai | https://seektool.ai/fr/new | AI tool directories | html |
| seofai.com | https://seofai.com/explore/?type=ai-tools&sort=latest | AI tool directories | html |
| showmebest.ai | https://showmebest.ai/sitemap.xml | AI tool directories | sitemap |
| submitaitools.org | https://submitaitools.org/sitemap.xml | AI tool directories | sitemap |
| supertools.therundown.ai | https://supertools.therundown.ai/feed | AI tool directories | rss |
| thataicollection.com | https://thataicollection.com/served-sitemap.xml | AI tool directories | sitemap |
| thetoolsverse.com | https://thetoolsverse.com/categories/latest-ai | AI tool directories | html |
| toolfio.com | https://toolfio.com/sitemap.xml | AI tool directories | sitemap |
| toolfolio.com | https://toolfolio.com/sitemap.xml | AI tool directories | sitemap |
| toolpilot.ai | https://www.toolpilot.ai/collections/new-ai-tools/products.json?limit=60 | AI tool directories | shopify_json |
| toolsfine.com | https://toolsfine.com/sitemap-core.xml | AI tool directories | sitemap |
| topaihubs.com | https://topaihubs.com/ | AI tool directories | html_cards |
| ufind.best | https://ufind.best/mcp | AI tool directories | mcp |
| verifiedtools.info | https://www.verifiedtools.info/sitemap.xml | AI tool directories | sitemap |

### SaaS and general tool directories (25)

| Name | URL | Category | Method |
| --- | --- | --- | --- |
| alterbase.co | https://alterbase.co/sitemap.xml | SaaS and general tool directories | sitemap |
| alternativeto.net | https://alternativeto.net/browse/new-apps/ | SaaS and general tool directories | html |
| appsumo.com | https://appsumo.com/collections/new/ | SaaS and general tool directories | html |
| confettisaas.com | https://confettisaas.com/sitemap.xml | SaaS and general tool directories | sitemap |
| devresourc.es | https://devresourc.es/feed.xml | SaaS and general tool directories | rss |
| directree.io | https://www.directree.io/new | SaaS and general tool directories | html |
| dododirectory.com | https://dododirectory.com/sitemap.xml | SaaS and general tool directories | sitemap |
| euroalternative.eu | https://euroalternative.eu/rss/tools.xml | SaaS and general tool directories | rss |
| featuredtool.com | https://featuredtool.com/sitemap.xml | SaaS and general tool directories | sitemap |
| findyoursaas.com | https://findyoursaas.com/sitemap/pages.xml | SaaS and general tool directories | sitemap |
| microsaasexamples.com | https://www.microsaasexamples.com/sitemap.xml | SaaS and general tool directories | sitemap |
| newtool.site | https://newtool.site/sitemap.xml | SaaS and general tool directories | sitemap |
| openalternative.co | https://openalternative.co/rss/tools.xml | SaaS and general tool directories | rss |
| promoteproject.com | https://www.promoteproject.com/sitemap/startups.xml | SaaS and general tool directories | sitemap |
| publicapis.dev | https://publicapis.dev/feed.xml | SaaS and general tool directories | rss |
| saasbison.com | https://saasbison.com/sitemap.xml | SaaS and general tool directories | sitemap |
| saasgrow.app | https://saasgrow.app/sitemap.xml | SaaS and general tool directories | sitemap |
| saashub.com | https://saashub.com/new | SaaS and general tool directories | html |
| scoutforge.net | https://scoutforge.net/sitemap.xml | SaaS and general tool directories | sitemap |
| submitmysaas.com | https://submitmysaas.com/sitemap.xml | SaaS and general tool directories | sitemap |
| thesaashub.com | https://thesaashub.com/sitemap.xml | SaaS and general tool directories | sitemap |
| toolfame.com | https://toolfame.com/sitemap.xml | SaaS and general tool directories | sitemap |
| toolfinder.co | https://toolfinder.com/tools/new | SaaS and general tool directories | html |
| uno.directory | https://uno.directory/sitemap.xml | SaaS and general tool directories | sitemap |
| versily.com | https://versily.com/rss/products.xml | SaaS and general tool directories | rss |

### Community and content platforms (3)

| Name | URL | Category | Method |
| --- | --- | --- | --- |
| dev.to | https://dev.to/api/articles?tag=showdev&per_page=30 | Community and content platforms | json_api |
| news.ycombinator.com | https://hn.algolia.com/api/v1/search_by_date?tags=show_hn | Community and content platforms | hn_api |
| producthunt.com | https://www.producthunt.com/feed | Community and content platforms | ph_graphql |

## Name and URL host differ

| Name | URL host |
| --- | --- |
| betalist.com | feeds.feedburner.com |
| peerpush.net | peerpush.com |
| toolfinder.co | toolfinder.com |
| news.ycombinator.com | hn.algolia.com |
