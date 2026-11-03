# launch-sources

[中文](#zh) · [English](#en) · [清单 / Catalog](#catalog)

**130 个公开信源，用来看新站发布和工具目录。**  
**130 public sources for new launches and tool directories.**

由 **范师傅（[@fanshifu](https://x.com/FanShifu)）** 整理。  
Curated by **范师傅 ([@fanshifu](https://x.com/FanShifu))**.

整理日期 / Prepared: 2026-11-03。共 130 条 / 130 entries。这是一份快照，不会自动更新。  
This is a snapshot. It is not updated automatically.

许可 / License: [MIT](LICENSE)。Copyright (c) 2026 范师傅 (Fan Shifu)。

| 文件 File | 内容 Content |
| --- | --- |
| `README.md` | 本说明 / this document |
| `sources.json` | 130 条 JSON 数组，每条只有四个字段 / JSON array of 130 objects, four fields each |
| `sources.csv` | 同一份表，UTF-8，无 BOM / the same table, UTF-8, no BOM |
| `LICENSE` | MIT License。Copyright (c) 2026 范师傅 (Fan Shifu)。 |

<a id="zh"></a>

## 中文

范师傅（[@fanshifu](https://x.com/FanShifu)）整理。

我每天用这 130 个公开地址看有什么新站。新品发布平台 58 个，AI 工具目录 44 个，SaaS 和通用工具目录 25 个，社区和内容平台 3 个。这 130 个是从 1000 多个目录站和发布站里筛出来、现在还能公开读取的来源。

仓库里是清单、这份说明和 MIT 许可。

### 字段

| 字段 | 含义 |
| --- | --- |
| `name` | 站点标识，多数是域名 |
| `url` | 公开读取地址 |
| `category` | 下面四类之一，值为中文 |
| `method` | 抓取方式代码 |

`sources.json` 是数组。每条对象只有这四个键，顺序固定为 `name`、`url`、`category`、`method`。

```json
{
  "name": "betalist.com",
  "url": "https://feeds.feedburner.com/BetaList",
  "category": "新品发布平台",
  "method": "rss"
}
```

`sources.csv` 用同样的列名和同样的顺序。类别按「新品发布平台、AI工具目录、SaaS/工具目录、社区/内容平台」排列，同一类里按名称排序，不区分大小写。

名称有时和 URL 的主机名不一样。BetaList 的订阅在 FeedBurner 上。其余不一致的条目见文末。

### 类别

| 类别 | 条数 | 在看什么 |
| --- | ---: | --- |
| `新品发布平台` | 58 | 新产品发布、每周上新、launch 列表 |
| `AI工具目录` | 44 | AI 工具导航和最新收录 |
| `SaaS/工具目录` | 25 | SaaS、独立开发者工具和通用目录 |
| `社区/内容平台` | 3 | Dev.to、Hacker News Show HN、Product Hunt |

字段里写的是左列的原文。`SaaS/工具目录` 就是 SaaS 和通用工具目录。

### 抓取方式

| method | 条数 | 含义 |
| --- | ---: | --- |
| `sitemap` | 60 | 公开 sitemap。和上一份对比，多出来的地址就是新页面。 |
| `html` | 37 | 公开列表页。 |
| `rss` | 18 | 公开 RSS 或 Atom。 |
| `mcp` | 5 | 公开 MCP 端点。清单里没有工具名、参数或凭证。 |
| `html_cards` | 4 | 列表页上重复出现的卡片。 |
| `json_api` | 3 | 公开 JSON。 |
| `shopify_json` | 1 | Shopify 店铺公开的 products.json。 |
| `hn_api` | 1 | Hacker News 的 Algolia 检索，只取 Show HN。 |
| `ph_graphql` | 1 | Product Hunt。这里公布的是公开 RSS，没有 GraphQL 查询，也没有凭证。 |

读取时先用现成的 API 和 Feed，再读列表页，然后用 sitemap 和上一份结果做差分。`method` 表示这个地址适合哪一种读法。

`ph_graphql` 这一条的 URL 是 `https://www.producthunt.com/feed`。

URL 上现有的查询参数是公开筛选：语言、排序、条数或标签。例如 `tag=showdev`、`per_page=30`、`limit=60`、`tags=show_hn`、`lg=en`、`sort=time_desc`。

### 使用

遵守每个站点自己的 robots.txt 和服务条款，并留出访问间隔。收录进这份清单，只说明该公开页面在观察范围内。商标和条款仍属于该站点。

### 范围

清单里是公开页面、公开 Feed、公开 sitemap 或公开接口。不含访问令牌、Cookie、账号、付费接口配置、内部路径或私有 IP。

### 许可

[MIT 许可证](LICENSE)。Copyright (c) 2026 范师傅 (Fan Shifu)。你可以复制、修改、分发这份清单，并在副本中保留版权声明和许可声明。各站点的商标仍属于该站点。

<a id="en"></a>

## English

Curated by 范师傅 ([@fanshifu](https://x.com/FanShifu)).

I use these 130 public addresses to see what launched. There are 58 new-product launch platforms, 44 AI tool directories, 25 SaaS and general tool directories, and 3 community or content sites. I screened more than 1,000 directory and launch sites and kept these 130, which can still be read in public.

This repository holds the list, this explanation, and the MIT license.

### Fields

| Field | Meaning |
| --- | --- |
| `name` | Site label, usually a domain |
| `url` | Public URL to read |
| `category` | One of the four categories below; the value is Chinese |
| `method` | Fetch-method code |

`sources.json` is an array. Each object has only these four keys, in this order: `name`, `url`, `category`, `method`.

```json
{
  "name": "betalist.com",
  "url": "https://feeds.feedburner.com/BetaList",
  "category": "新品发布平台",
  "method": "rss"
}
```

`sources.csv` uses the same columns and the same order. Categories follow the order launch platforms, AI directories, SaaS and general directories, then community sites. Inside a category, rows are sorted by name, case-insensitive.

The name is sometimes a different host from the URL. The BetaList feed is on FeedBurner. The other mismatches are listed at the end.

### Categories

| Category value | Count | Meaning |
| --- | ---: | --- |
| `新品发布平台` | 58 | New-product launch platforms |
| `AI工具目录` | 44 | AI tool directories |
| `SaaS/工具目录` | 25 | SaaS and general tool directories |
| `社区/内容平台` | 3 | Community and content platforms |

The value stored in the files is the Chinese string in the first column. `SaaS/工具目录` means SaaS and general tool directories.

### Fetch methods

| method | Count | Meaning |
| --- | ---: | --- |
| `sitemap` | 60 | Public sitemap. URLs that were not in the previous copy are the new pages. |
| `html` | 37 | Public listing page. |
| `rss` | 18 | Public RSS or Atom feed. |
| `mcp` | 5 | Public MCP endpoint. No tool name, arguments, or credentials are included. |
| `html_cards` | 4 | Repeated cards on a listing page. |
| `json_api` | 3 | Public JSON. |
| `shopify_json` | 1 | Public Shopify products.json for a collection. |
| `hn_api` | 1 | Hacker News search on Algolia, limited to Show HN. |
| `ph_graphql` | 1 | Product Hunt. The URL in this list is the public RSS feed. No GraphQL query and no credential is included. |

Read an existing API or feed first, then a listing page, then diff a sitemap against the previous copy. `method` says which of those fits the URL.

The `ph_graphql` row points at `https://www.producthunt.com/feed`.

Query strings already on these URLs are public filters: language, sort, page size, or a tag. Examples: `tag=showdev`, `per_page=30`, `limit=60`, `tags=show_hn`, `lg=en`, `sort=time_desc`.

### Use

Follow each site's robots.txt and terms, and leave a polite interval between requests. A row means the public page is in this watch list. Trademarks and terms stay with that site.

### Scope

The list contains public pages, public feeds, public sitemaps, or public APIs. It does not include access tokens, cookies, accounts, paid-API configuration, internal paths, or private IP addresses.

### License

[MIT License](LICENSE). Copyright (c) 2026 范师傅 (Fan Shifu). You can copy, modify, and distribute this list if you keep the copyright notice and the permission notice. Trademarks stay with each site.

<a id="catalog"></a>

## 清单 / Catalog

排序与 `sources.json`、`sources.csv` 相同。  
Same order as `sources.json` and `sources.csv`.

### 新品发布平台 / New-product launch platforms (58)

| 名称 Name | URL | 类别 Category | 抓取方式 Method |
| --- | --- | --- | --- |
| 1000.tools | https://1000.tools/sitemap.xml | 新品发布平台 | sitemap |
| altern.ai | https://altern.ai/recent | 新品发布平台 | html |
| auraplusplus.com | https://auraplusplus.com/launches | 新品发布平台 | html |
| betalist.com | https://feeds.feedburner.com/BetaList | 新品发布平台 | rss |
| buildvoyage.com | https://buildvoyage.com/sitemaps/pages.xml | 新品发布平台 | sitemap |
| businesshunt.co | https://businesshunt.co/sitemap.xml | 新品发布平台 | sitemap |
| curlship.com | https://curlship.com/sitemap.xml | 新品发布平台 | sitemap |
| devhunt.org | https://devhunt.org/upcoming | 新品发布平台 | html |
| fazier.com | https://fazier.com/ | 新品发布平台 | html |
| findly.tools | https://findly.tools/sitemap.xml | 新品发布平台 | sitemap |
| firsto.co | https://firsto.co/sitemap.xml | 新品发布平台 | sitemap |
| founder.best | https://www.founder.best/api/mcp | 新品发布平台 | mcp |
| foundrlist.com | https://www.foundrlist.com/feeds/products.xml | 新品发布平台 | rss |
| griv.io | https://griv.io/sitemap | 新品发布平台 | sitemap |
| huntifyai.com | https://huntifyai.com/tools?sort=time_desc | 新品发布平台 | html |
| huzzler.so | https://huzzler.so/sitemap.xml | 新品发布平台 | sitemap |
| ideakiln.com | https://ideakiln.com/ideas/today | 新品发布平台 | html |
| indiehub.best | https://indiehub.best/sitemap.xml | 新品发布平台 | sitemap |
| indiepa.ge | https://indiepa.ge/new | 新品发布平台 | html |
| indietool.io | https://www.indietool.io/sitemap.xml | 新品发布平台 | sitemap |
| launchboosts.com | https://launchboosts.com/ | 新品发布平台 | html_cards |
| launchbuff.com | https://launchbuff.com/sitemap.xml | 新品发布平台 | sitemap |
| launchigniter.com | https://launchigniter.com/sitemap.xml | 新品发布平台 | sitemap |
| launchvault.dev | https://www.launchvault.dev/trending | 新品发布平台 | html |
| microlaunch.net | https://microlaunch.net/sitemap-0.xml | 新品发布平台 | sitemap |
| nicklaunches.com | https://nicklaunches.com/ | 新品发布平台 | html |
| open-launch.com | https://open-launch.com/sitemap.xml | 新品发布平台 | sitemap |
| openhunts.com | https://openhunts.com/sitemap.xml | 新品发布平台 | sitemap |
| peerpush.net | https://peerpush.com/api/mcp | 新品发布平台 | mcp |
| pitchwall.co | https://pitchwall.co/rss | 新品发布平台 | rss |
| productfame.com | https://productfame.com/trending | 新品发布平台 | html |
| productwatch.io | https://productwatch.io/launches/day | 新品发布平台 | html |
| rankinpublic.xyz | https://rankinpublic.xyz/sitemap-0.xml | 新品发布平台 | sitemap |
| saascity.io | https://saascity.io/live | 新品发布平台 | html |
| saasfame.com | https://saasfame.com/sitemap.xml | 新品发布平台 | sitemap |
| saashunt.best | https://saashunt.best/sitemap/0.xml | 新品发布平台 | sitemap |
| scrolllaunch.com | https://www.scrolllaunch.com/api/mcp | 新品发布平台 | mcp |
| shinylaunch.com | https://shinylaunch.com/latest | 新品发布平台 | html |
| shipboost.io | https://shipboost.io/launches/weekly | 新品发布平台 | html |
| shipstry.com | https://shipstry.com/rss.xml | 新品发布平台 | rss |
| similarlabs.com | https://similarlabs.com/zh/launches | 新品发布平台 | html |
| smollaunch.com | https://smollaunch.com/api/v1/products | 新品发布平台 | json_api |
| startupbase.io | https://startupbase.io/launches | 新品发布平台 | html |
| startupfa.st | https://www.startupfa.st/trending | 新品发布平台 | html |
| startupstash.com | https://startupstash.com/page-sitemap.xml | 新品发布平台 | sitemap |
| submithunt.com | https://www.submithunt.com/sitemap.xml | 新品发布平台 | sitemap |
| sumodir.com | https://sumodir.com/sitemap.xml | 新品发布平台 | sitemap |
| tinyhunt.dev | https://tinyhunt.dev/sitemap/0.xml | 新品发布平台 | sitemap |
| tinylaunch.com | https://tinylaunch.com/sitemap.xml | 新品发布平台 | sitemap |
| tinylaunchpad.com | https://tinylaunchpad.com/sitemap.xml | 新品发布平台 | sitemap |
| tinystartups.com | https://www.tinystartups.com/today | 新品发布平台 | html |
| toolatlas.io | https://toolatlas.io/launches | 新品发布平台 | html |
| toolhunter.ai | https://toolhunter.ai/sitemap.xml | 新品发布平台 | sitemap |
| tools.launchllama.co | https://tools.launchllama.co/sitemap.xml | 新品发布平台 | sitemap |
| turbo0.com | https://turbo0.com/collection/new-this-month | 新品发布平台 | html |
| uneed.best | https://mcp.uneed.best/mcp | 新品发布平台 | mcp |
| vibecodinglist.com | https://vibecodinglist.com/sitemap.xml | 新品发布平台 | sitemap |
| whatlaunched.today | https://whatlaunched.today/feed.xml | 新品发布平台 | rss |

### AI工具目录 / AI tool directories (44)

| 名称 Name | URL | 类别 Category | 抓取方式 Method |
| --- | --- | --- | --- |
| aiagentsdirectory.com | https://aiagentsdirectory.com/sitemap.xml | AI工具目录 | sitemap |
| aibesttop.com | https://aibesttop.com/sitemap.xml | AI工具目录 | sitemap |
| aidirectori.es | https://www.aidirectori.es/sitemaps/static.xml | AI工具目录 | sitemap |
| aihubs.ai | https://aihubs.ai/sitemap.xml | AI工具目录 | sitemap |
| aistage.net | https://aistage.net/tools/latest | AI工具目录 | html |
| aitoolly.com | https://aitoolly.com/ai-news/rss.xml | AI工具目录 | rss |
| aitoolnet.com | https://www.aitoolnet.com/new | AI工具目录 | html_cards |
| aitools.inc | https://aitools.inc/sitemap.xml | AI工具目录 | sitemap |
| aitoolsclub.com | https://aitoolsclub.com/rss/ | AI工具目录 | rss |
| aitoolsdirectory.com | https://aitoolsdirectory.com/items.rss | AI工具目录 | rss |
| aitooltrek.com | https://aitooltrek.com/sitemap.xml | AI工具目录 | sitemap |
| aivalley.ai | https://aivalley.ai/feed/ | AI工具目录 | rss |
| aiwith.me | https://aiwith.me/sitemap.xml | AI工具目录 | sitemap |
| aixploria.com | https://www.aixploria.com/feed | AI工具目录 | rss |
| bestofai.com | https://bestofai.com/new-tools | AI工具目录 | html |
| codehype.ai | https://www.codehype.ai/v1/launches | AI工具目录 | json_api |
| creati.ai | https://creati.ai/ai-tools/new/ | AI工具目录 | html |
| dang.ai | https://dang.ai/new | AI工具目录 | html |
| firstlook.tools | https://firstlook.tools/sitemap.xml | AI工具目录 | sitemap |
| futurepedia.io | https://www.futurepedia.io/sitemap.xml | AI工具目录 | sitemap |
| futuretools.io | https://futuretools.io/sitemaps/pages.xml | AI工具目录 | sitemap |
| goodaitools.com | https://goodaitools.com/latest | AI工具目录 | html |
| gptdemo.net | https://www.gptdemo.net/gpt/today?lg=en | AI工具目录 | html |
| iuu.ai | https://iuu.ai/sitemap.xml | AI工具目录 | sitemap |
| magicbox.tools | https://magicbox.tools/latest | AI工具目录 | html |
| mossai.org | https://mossai.org/ | AI工具目录 | html_cards |
| nxgntools.com | https://www.nxgntools.com/launching | AI工具目录 | html |
| poweredbyai.app | https://poweredbyai.app/latest-tools | AI工具目录 | html |
| rankyourai.com | https://rankyourai.com/rss.xml/ | AI工具目录 | rss |
| saasaitools.com | https://saasaitools.com/feed/ | AI工具目录 | rss |
| seektool.ai | https://seektool.ai/fr/new | AI工具目录 | html |
| seofai.com | https://seofai.com/explore/?type=ai-tools&sort=latest | AI工具目录 | html |
| showmebest.ai | https://showmebest.ai/sitemap.xml | AI工具目录 | sitemap |
| submitaitools.org | https://submitaitools.org/sitemap.xml | AI工具目录 | sitemap |
| supertools.therundown.ai | https://supertools.therundown.ai/feed | AI工具目录 | rss |
| thataicollection.com | https://thataicollection.com/served-sitemap.xml | AI工具目录 | sitemap |
| thetoolsverse.com | https://thetoolsverse.com/categories/latest-ai | AI工具目录 | html |
| toolfio.com | https://toolfio.com/sitemap.xml | AI工具目录 | sitemap |
| toolfolio.com | https://toolfolio.com/sitemap.xml | AI工具目录 | sitemap |
| toolpilot.ai | https://www.toolpilot.ai/collections/new-ai-tools/products.json?limit=60 | AI工具目录 | shopify_json |
| toolsfine.com | https://toolsfine.com/sitemap-core.xml | AI工具目录 | sitemap |
| topaihubs.com | https://topaihubs.com/ | AI工具目录 | html_cards |
| ufind.best | https://ufind.best/mcp | AI工具目录 | mcp |
| verifiedtools.info | https://www.verifiedtools.info/sitemap.xml | AI工具目录 | sitemap |

### SaaS/工具目录 / SaaS and general tool directories (25)

| 名称 Name | URL | 类别 Category | 抓取方式 Method |
| --- | --- | --- | --- |
| alterbase.co | https://alterbase.co/sitemap.xml | SaaS/工具目录 | sitemap |
| alternativeto.net | https://alternativeto.net/browse/new-apps/ | SaaS/工具目录 | html |
| appsumo.com | https://appsumo.com/collections/new/ | SaaS/工具目录 | html |
| confettisaas.com | https://confettisaas.com/sitemap.xml | SaaS/工具目录 | sitemap |
| devresourc.es | https://devresourc.es/feed.xml | SaaS/工具目录 | rss |
| directree.io | https://www.directree.io/new | SaaS/工具目录 | html |
| dododirectory.com | https://dododirectory.com/sitemap.xml | SaaS/工具目录 | sitemap |
| euroalternative.eu | https://euroalternative.eu/rss/tools.xml | SaaS/工具目录 | rss |
| featuredtool.com | https://featuredtool.com/sitemap.xml | SaaS/工具目录 | sitemap |
| findyoursaas.com | https://findyoursaas.com/sitemap/pages.xml | SaaS/工具目录 | sitemap |
| microsaasexamples.com | https://www.microsaasexamples.com/sitemap.xml | SaaS/工具目录 | sitemap |
| newtool.site | https://newtool.site/sitemap.xml | SaaS/工具目录 | sitemap |
| openalternative.co | https://openalternative.co/rss/tools.xml | SaaS/工具目录 | rss |
| promoteproject.com | https://www.promoteproject.com/sitemap/startups.xml | SaaS/工具目录 | sitemap |
| publicapis.dev | https://publicapis.dev/feed.xml | SaaS/工具目录 | rss |
| saasbison.com | https://saasbison.com/sitemap.xml | SaaS/工具目录 | sitemap |
| saasgrow.app | https://saasgrow.app/sitemap.xml | SaaS/工具目录 | sitemap |
| saashub.com | https://saashub.com/new | SaaS/工具目录 | html |
| scoutforge.net | https://scoutforge.net/sitemap.xml | SaaS/工具目录 | sitemap |
| submitmysaas.com | https://submitmysaas.com/sitemap.xml | SaaS/工具目录 | sitemap |
| thesaashub.com | https://thesaashub.com/sitemap.xml | SaaS/工具目录 | sitemap |
| toolfame.com | https://toolfame.com/sitemap.xml | SaaS/工具目录 | sitemap |
| toolfinder.co | https://toolfinder.com/tools/new | SaaS/工具目录 | html |
| uno.directory | https://uno.directory/sitemap.xml | SaaS/工具目录 | sitemap |
| versily.com | https://versily.com/rss/products.xml | SaaS/工具目录 | rss |

### 社区/内容平台 / Community and content platforms (3)

| 名称 Name | URL | 类别 Category | 抓取方式 Method |
| --- | --- | --- | --- |
| dev.to | https://dev.to/api/articles?tag=showdev&per_page=30 | 社区/内容平台 | json_api |
| news.ycombinator.com | https://hn.algolia.com/api/v1/search_by_date?tags=show_hn | 社区/内容平台 | hn_api |
| producthunt.com | https://www.producthunt.com/feed | 社区/内容平台 | ph_graphql |

### 名称和 URL 主机名不一致 / Name and URL host differ

| 名称 Name | URL 主机 Host |
| --- | --- |
| betalist.com | feeds.feedburner.com |
| peerpush.net | peerpush.com |
| toolfinder.co | toolfinder.com |
| news.ycombinator.com | hn.algolia.com |
