# The Definitive Guide to Next-Gen Sports Tracking Data
## Access, Sources, and Predictive Value Across 11 Major Sports

**Every major sport now generates millions of data points per game — but almost none of it reaches the public in raw form.** Across 11 sports, the pattern is consistent: leagues deploy cutting-edge tracking systems (RFID chips, optical cameras, GPS sensors, computer vision), yet raw coordinate-level data stays locked behind enterprise licensing deals. The real edge for sports modelers lies in knowing exactly which derived metrics are publicly accessible, which require paid subscriptions, and which free open-source tools aggregate data from multiple sources into analysis-ready formats. This guide catalogs every significant source of advanced analytics data across NFL, NBA, MLB, NHL, soccer, tennis, golf, MMA, F1, cricket, and horse racing — with practical details on access, format, pricing, and predictive value.

---

## NFL: nflfastR is the Single Best Free Resource in All of Sports Analytics

The NFL's tracking infrastructure uses **Zebra Technologies RFID tags** in shoulder pads (2 per player) and Wilson footballs, tracked at 10–12 Hz via 22–24 ultra-wideband antennas per stadium with sub-6-inch accuracy. This generates **250–300 million data points per season**. But raw tracking data is exclusively available to the 32 NFL clubs and authorized partners. The public gets aggregated stats via nextgenstats.nfl.com and limited raw data through the annual **NFL Big Data Bowl** on Kaggle (CSV files with frame-level X/Y/speed/acceleration for all 22 players — the only public source of raw NFL tracking data).

### Key Sources

**NFL Next Gen Stats** (nextgenstats.nfl.com) — Free aggregate leaderboards. Metrics include completion probability (CP), completion percentage over expected (CPOE), expected rushing yards (RYOE), separation distance, time to throw, aggressiveness, coverage classification, and pressure probability. No API exists. NFL+ Premium (~$14.99/month) adds interactive dashboards but not raw data.

**nflfastR / nflverse** (nflfastr.com, github.com/nflverse) — **The gold standard for public NFL analytics.** This free, open-source ecosystem provides **339 columns per play** from 1999 to present, including EPA (Expected Points Added), WPA (Win Probability Added), CPOE, xYAC, completion probability, pass rate over expected, and the DAKOTA composite metric (the single best predictor of next-year QB EPA/play). Available in R (`nflreadr::load_pbp()`), Python (`nfl_data_py`), and direct CSV/Parquet downloads. Updated nightly during the season. MIT licensed with zero restrictions.

**PFF (Pro Football Focus)** (pff.com) — Human-graded play-level data on a 0–100 scale for every player on every play since **2006**. Consumer subscription runs $10–35/month; enterprise B2B licensing (SQL/CSV/XML feeds) requires custom pricing. All 32 NFL teams and 100+ NCAA programs are clients. PFF grades are descriptive rather than predictive in isolation, but the underlying charting data (pressures, coverage assignments, play concepts) is invaluable.

**ESPN's undocumented API** — Free JSON endpoints at `sports.core.api.espn.com` requiring no authentication. Returns QBR (2006+), play-by-play, win probabilities, scores, and standings. Widely used but unofficial — endpoints can change without notice. Community documentation at github.com/pseudo-r/Public-ESPN-API.

**Football Outsiders DVOA** — The best opponent-adjusted team efficiency metric, calculated from **1981 to present**. Now behind FTN Fantasy's paywall after Football Outsiders shut down in August 2023. No API. Updated weekly (Tuesdays), not real-time.

### NFL Source Comparison Table

| Source | Free? | API? | Format | Historical Depth | Real-time? |
|--------|-------|------|--------|-----------------|------------|
| nflfastR/nflverse | ✅ Free | Open-source packages | CSV/Parquet | 1999+ | Nightly |
| NFL Next Gen Stats | ✅ Aggregate only | No | HTML | 2016+ | Delayed |
| NFL Big Data Bowl | ✅ Free | Kaggle download | CSV | 2–3 seasons | No |
| PFF | $10–35/mo consumer | B2B only (SQL/CSV) | SQL/CSV/XML | 2006+ | Near real-time |
| ESPN API | ✅ Free | Undocumented REST | JSON | 2006+ | Live |
| DVOA (FTN) | Paid subscription | No | HTML | 1981+ | Weekly |
| Sportradar | Enterprise pricing | REST v7 | JSON/XML | Deep | Real-time |
| Pro Football Reference | Free (Stathead $8/mo) | No | HTML | 1920+ | Nightly |

---

## NBA: 3D Skeletal Tracking Arrived in 2023, But Raw Data Remains Locked Away

The NBA transitioned to **Hawk-Eye's optical tracking system** (a Sony subsidiary) league-wide in 2023–24, deploying **14 cameras per arena** that capture **29 skeletal keypoints per player** in 3D — a massive upgrade from Second Spectrum's previous 2D "center of mass" tracking (6 cameras). This enables automated analysis of shot contests via hand proximity, movement biomechanics, and precise ball trajectory. However, raw coordinate-level data remains exclusively available to the 30 NBA teams and licensed partners (Sportradar is the NBA's exclusive data distributor).

### Key Sources

**stats.nba.com** — The undocumented JSON API remains the richest free source. Endpoints cover player tracking (speed, distance, touches, drives), hustle stats (deflections, loose balls, charges drawn), shooting by defender distance, Synergy play-type data, matchup assignments, and play-by-play. The **nba_api Python package** (github.com/swar/nba_api, 3.4k+ stars) wraps 100+ endpoints. No authentication required, but Cloudflare rate limiting blocks aggressive requests — use 1–2 second delays. Cloud-hosted IPs are frequently banned. Tracking data available from **2013–14** (SportVU era), with play-by-play back to **1996–97**.

**Archived SportVU raw tracking data** — The only publicly available raw NBA tracking data. Community-preserved on GitHub (`neilmj/nba-movement-data`) and Hugging Face (`dcayton/nba_tracking_data_15_16`) from the 2015–16 season. JSON files with X/Y coordinates per moment for all 10 players, referees, and ball.

**Key independent analytics platforms:**
- **Cleaning the Glass** ($5–7.50/month) — Filters out garbage time and heaves
- **BBall Index** — LEBRON metric, free dashboard
- **Dunks & Threes** — EPM (one of the best public impact metrics), free basic tier
- **PBPStats** — Unique WOWY combinations, free with Patreon tracking tier
- **Second Spectrum** (acquired by Genius Sports for $200M) — NBA's analytics and broadcast augmentation provider, offering quantified shot quality (qSQ) and shooter impact (qSI) metrics to teams

For predictive modeling, **EPM** (Estimated Plus-Minus) and **LEBRON** are the strongest public single-number impact metrics. Shot quality models and defensive matchup data from stats.nba.com provide the most actionable tracking-derived edge.

---

## MLB: Baseball Savant is the Most Generous Free Tracking Data Portal in Professional Sports

MLB's **Statcast system** (powered by Hawk-Eye since 2020, replacing TrackMan) captures **90+ fields per pitch** and makes nearly all of it available for free at baseballsavant.mlb.com. This is unmatched generosity in professional sports data access.

### Key Sources

**Baseball Savant / Statcast** — Free CSV downloads with no registration. Pitch-level data includes release speed, spin rate, movement, release extension, spin axis. Batted ball data includes exit velocity, launch angle, hit distance, estimated batting average (xBA), expected weighted on-base average (xwOBA). Player tracking captures sprint speed, bat speed, swing length, attack angle. Fielding metrics include Outs Above Average (OAA), arm strength, pop time, route efficiency. The Statcast Search tool serves CSV via URL parameters (effectively an undocumented API), limited to **25,000–40,000 rows per query**. Full Statcast data available from **2015**, with PITCHf/x data back to **2008**.

**pybaseball** (github.com/jldbc/pybaseball) — The essential Python library aggregating Statcast, FanGraphs, and Baseball Reference data. Returns pandas DataFrames with up to **334 features per player-season** from FanGraphs. Free, MIT licensed. Automatically handles Savant's row limits by breaking queries into 5-day chunks.

**MLB Stats API** (statsapi.mlb.com) — Free, no-authentication REST API returning JSON. Provides **true real-time** pitch-by-pitch game feeds. Does not include Statcast-specific metrics (spin rate, exit velocity) — for those, use Baseball Savant. The `MLB-StatsAPI` Python wrapper simplifies access.

**FanGraphs** (fangraphs.com) — **300+ metrics per player-season** including fWAR, wRC+, FIP, xFIP, SIERA, Stuff+, plate discipline stats, and batted ball data. Free to browse; membership ($15/month or $80/year) required for full custom CSV exports. Data back to **1871** for traditional stats.

**Retrosheet** (retrosheet.org) — Play-by-play event files for most seasons **1911–2024**, freely available under a permissive license that explicitly allows commercial use. The only requirement is copyright attribution. CSV files covering 16 million+ plays.

### Predictive vs. Descriptive Value
Statcast's expected stats (xBA, xSLG, xwOBA) are **marginally more predictive** than traditional stats but not dramatically so. xwOBA's R² for predicting future wOBA is ~0.218 vs. ~0.191 for actual wOBA. They are best used as descriptive tools isolating contact quality. **FIP and SIERA** remain strong pitching predictors. **Barrel rate and hard-hit rate** are among the most stable and predictive batted-ball metrics.

---

## NHL: MoneyPuck's Free CSV Downloads Are the Hidden Gem of Hockey Analytics

The NHL deployed its **Edge IQ tracking system** league-wide in 2021–22 using **14 infrared cameras** per rink plus sensors in pucks (60 Hz) and player jerseys (15 Hz), generating ~1 million 3D coordinates per game. Public metrics include skating speed, distance covered, shot speed, zone time, and ML-powered Ice Tilt (territorial control) and Opportunity Analysis (shot difficulty). The NHL API includes 66 undocumented EDGE endpoints accessible without authentication at `api-web.nhle.com/v1/`.

### Key Sources

**MoneyPuck** (moneypuck.com) — **The most valuable free hockey analytics resource.** Offers downloadable CSVs with **124 attributes per shot** covering 1.7M+ shots from 2007–08 to present, including xGoals probability, flurry-adjusted xG, and rebound probability. Also provides season-level player data, game-level team data, and a detailed data dictionary. Their expected goals model uses gradient boosting with 13+ features. Updated nightly. Free with credit requirement.

**Natural Stat Trick** (naturalstattrick.com) — Comprehensive Corsi, Fenwick, scoring chances, high-danger chances, xG, and on-ice/off-ice data. Filterable by game state (5v5, PP, PK, etc.). CSV export available from stat pages. Mostly free; Patreon tiers add 4–5 seasons of data viewing. Data from **2007–08**.

**Evolving Hockey** (evolving-hockey.com, $5/month) — Home of **GAR (Goals Above Replacement)** and **WAR**, the most comprehensive public player-valuation framework in hockey. Also provides RAPM, xGAR, contract projections, and live in-game win probability (updated 30x/hour). Data from 2007–08.

**The NHL API** (api-web.nhle.com) — Free, no authentication, JSON. Covers schedules, play-by-play with coordinates, EDGE tracking data, standings, and records. Community documentation at github.com/Zmalski/NHL-API-Reference. 500+ endpoints across web, stats, and records base URLs. Play-by-play from **2007–08**; schedule data from **1918**.

**Sportlogiq** ($100K+/year) — The only provider generating truly novel data via computer vision, with 500+ metrics including zone entries/exits, passing networks, and micro-events invisible in play-by-play data.

Almost all public hockey analytics sites derive from the same NHL play-by-play data. The differentiation is in modeling: **xGF% is more predictive than CF% (Corsi) over any sample size**, and **flurry-adjusted xG** (MoneyPuck) is more repeatable than raw xG.

---

## Soccer: The January 2026 FBref Data Loss Fundamentally Reshaped the Free Analytics Landscape

A critical development occurred in **January 2026**: Opta/Stats Perform terminated their data agreement with FBref, forcing the **removal of all advanced statistics** (xG, xA, progressive passes, pressures, shot-creating actions, and dozens more) from what was the single best free source for soccer analytics globally. This was linked to Opta's exclusive FIFA World Cup 2026 betting data deal. The free soccer data landscape has been dramatically diminished.

### Key Sources

**StatsBomb** (statsbomb.com) now stands as the most important accessible source. Their **open data** (github.com/statsbomb/open-data) provides JSON files with **3,400+ events per match** — double Opta's ~1,600 — plus **360 freeze-frame data** capturing all visible player positions at every event. Coverage includes FIFA World Cups 2018/2022, Euro 2020/2024, select La Liga and Champions League seasons, and women's leagues. The `statsbombpy` Python and `StatsBombR` R libraries provide easy access. Paid data covers 170+ competitions.

**Understat** (understat.com) — Now the best remaining free source for xG data, covering **6 leagues** (EPL, La Liga, Serie A, Bundesliga, Ligue 1, Russian Premier League) from 2014–15. Their neural network xG model runs on 100,000+ shots with 10+ parameters. Data is embedded as JSON in page source, making it effectively an unofficial API. Python (`understatapi`) and R (`understatr`) wrappers exist.

**Tracking data remains entirely locked behind commercial providers:**
- **Hawk-Eye** (EPL, UEFA, FIFA) — 25fps positional data for all 22 players plus the ball
- **ChyronHego/Tracab** — La Liga and others
- **Sportec Solutions** (Bundesliga subsidiary) — 3.6M data points per match
- **SkillCorner** — Broadcast-derived tracking via computer vision for 120+ competitions (10 open-data A-League matches on GitHub)

**Opta/Stats Perform** (enterprise-only) remains the industry's backbone, feeding data to WhoScored, FotMob, SofaScore, and formerly FBref. Licensing runs tens to hundreds of thousands of dollars annually.

**Wyscout** (Hudl, from €299/year for scouts) covers 600+ competitions with an OpenAPI 3.0–compliant REST API.

### Predictive Value
**Team xG differential is a significantly better predictor of future results than actual goal differential.** Expected threat (xT) and on-ball value (OBV) models offer richer possession-valuation frameworks than xG alone but require event data access. The `socceraction` Python library implements xT openly. **PPDA** (passes per defensive action) is the best freely available pressing metric, accessible via Understat.

---

## Tennis: Niche Sport with Surprisingly Rich Open Data

Tennis data lives primarily in **Jeff Sackmann's GitHub repositories** (github.com/JeffSackmann) — the gold standard for open tennis analytics:

- **`tennis_atp`** (1.4k stars) — Match results from **1968**, rankings from **1985**, match stats from **1991** in CSV format
- **`tennis_MatchChartingProject`** — Crowdsourced shot-by-shot data for 17,000+ matches
- **`tennis_slam_pointbypoint`** — Grand Slam point-level data from 2011 onward

All are CC BY-NC-SA 4.0 licensed and frequently updated during tournaments.

Hawk-Eye's raw ball-tracking data (3D trajectory, serve speed, placement, spin, player skeletal tracking via 29-point SkeleTRACK) is captured at all Grand Slams and ATP Masters events but is **not publicly available** — tournaments own the data. A workaround: the `courtvisionpython` library extracts summary tracking data from Australian Open and Roland Garros "Court Vision" web applets (JSON, available for AO 2020+ and RG 2019+).

---

## Golf: ShotLink and DataGolf

Golf analytics center on **ShotLink**, the PGA Tour's shot-level tracking system generating 256,000+ data points per tournament week across 28,000 players and 21 million+ shot-level entries. Raw ShotLink data is proprietary but available to ~90 academics from 65+ universities through the ShotLink Intelligence academic program.

**DataGolf** (datagolf.com) is the best public golf analytics platform by a wide margin. For **$30/month** (Scratch PLUS), it provides:
- REST API access to round-level strokes-gained data from **22 global tours** (PGA, DP World, LIV, Korn Ferry, Japan, Korea, and more)
- Pre-tournament probabilistic predictions
- Live in-tournament win probability
- Historical odds archives
- Course-fit tools and DFS data
- JSON and CSV formats

An unofficial Python client exists (`coreyjs/data-golf-api`). **Strokes gained** (developed by Mark Broadie at Columbia) is the single most predictive framework in golf analytics — SG: Tee-to-Green is the strongest predictor of future performance.

---

## MMA and UFC: A Data Desert with Scraping as the Only Viable Path

MMA analytics is the least developed major-sport data ecosystem. **UFCStats.com** (powered by FightMetric, the UFC's official stats provider) is the primary source, offering **125+ statistical categories** per fight including significant strikes by target (head/body/leg) and position (distance/clinch/ground), takedowns, control time, knockdowns, and submission attempts. Historical data goes back to **UFC 28 (November 2000)**. There is **no official API** — all access requires scraping static HTML pages.

### Key Resources
- **`Greco1899/scrape_ufc_stats`** on GitHub — Auto-updates daily via GCP Cloud Run, producing 6 CSV files
- **Kaggle** — Multiple ready-to-analyze datasets with 120+ features per fight
- **BestFightOdds.com** — Deep archive of historical betting odds with line movement (essential for predictive modeling)
- **SportsDataIO** — Best documented professional API option (free trial, paid production)
- **Sportradar MMA API** — Enterprise-level, comprehensive fight data

---

## Formula 1: FastF1 Delivers Telemetry Data That Would Cost Millions in Other Sports

F1 is unique in that **detailed car telemetry** — speed, RPM, gear, throttle position, brake application, DRS status, and X/Y/Z coordinates — is accessible through open-source tools.

### Key Sources

**FastF1** (github.com/theOehrly/Fast-F1) — Python library tapping F1's live timing SignalR stream to provide lap-by-lap sector times, speed traps, tire compounds, weather data, and per-sample telemetry at ~3.7 Hz. Data available from **2018 onward**.

**OpenF1** (openf1.org) — Cleanest REST API with **18 endpoints** including car data, intervals, laps, pit stops, stints, race control messages, team radio recordings, and weather. Historical data is free (no auth); real-time requires paid subscription. JSON and CSV formats. Rate limit: 3 requests/second free tier.

**Jolpica-F1** (api.jolpi.ca/ergast/f1/) — The production-ready Ergast replacement — free, no authentication, backward-compatible URL structure (just swap the domain). Covers all F1 results, standings, lap times, and pit stops from **1950**. Rate limit: 200 requests/hour.

---

## Cricket: CricSheet is the Open-Source Jewel, Hawkeye Data Stays Locked

**CricSheet** (cricsheet.org) provides **free, open ball-by-ball data** for 21,000+ matches across 30+ competitions including all internationals, IPL, BBL, CPL, PSL, The Hundred, and more. Available in **JSON, YAML, and CSV** with 33 columns per delivery. Updated within days of matches. No restrictions on use. The R package `cricketdata` includes a `fetch_cricsheet()` function for programmatic access.

**ESPNcricinfo Statsguru** (stats.espncricinfo.com) offers the deepest historical cricket database — all international matches from the **first Test in 1877**. Its query engine supports filtering by team, opposition, venue, batting position, result, and time span. No API, but Python (`cricguru`) and R (`statsguRu`) scrapers exist.

**Hawkeye** captures 3D ball trajectory, pitch maps, spin rate, variable bounce, and LBW predictions using 6+ high-speed cameras, but this data is **entirely proprietary** — licensed only to broadcasters (Sky Sports, Star Sports), the ICC for DRS, and analytics firms like CricViz.

**CricViz** builds advanced metrics (expected wickets, expected average, control ratings, match win probability) on top of Hawkeye and Opta event data but is enterprise-only.

---

## Horse Racing: PDFs and Paywalls Dominate, But GPS Tracking is Emerging

Horse racing data is the most commercially guarded ecosystem. **Equibase** (equibase.com), the official North American database, deliberately publishes past performances as **anti-scraping PDFs** with obfuscated character encoding. Results cover every North American track since 1976. A free 2023 research dataset was released for development purposes.

### Key Sources

**Daily Racing Form** (drf.com) — Primary paid platform ($4.25–6.35/card), offering Beyer Speed Figures (the industry standard since 1992, human-calculated, exclusively DRF), TimeformUS pace-adjusted figures, and a **REST API via DRF Data Services** for programmatic access.

**Brisnet** (brisnet.com) — Machine-readable comma-delimited "ALL-Ways" data files for database handicapping software.

**Total Performance Data** (totalperformancedata.com) — Tracks 100,000+ races via GPS at 12+ US and UK tracks, providing real-time position, velocity, and stride frequency data via a **commercial REST API** (JSON format). This data — showing how a horse ran its race in segments rather than just final time — represents the biggest untapped predictive edge in the sport. Equibase has begun incorporating TPD GPS data into official charts.

---

## Which Advanced Stats Actually Predict? A Cross-Sport Synthesis

The distinction between descriptive and predictive metrics matters enormously for modeling. Across sports, **process metrics** (how something happened) consistently outperform **outcome metrics** (what happened) in forecasting.

| Sport | Most Predictive Metric(s) | Key Insight |
|-------|--------------------------|-------------|
| **NFL** | DAKOTA (EPA + CPOE composite) | Best public predictor of next-year QB performance |
| **NBA** | Multi-year RAPM, EPM | On/off data requires 1,000+ minutes to stabilize |
| **MLB** | Barrel rate, hard-hit rate, FIP | FIP outpredicts ERA; xwOBA marginally better than wOBA |
| **NHL** | xGF%, flurry-adjusted xG | PDO regresses hard toward 1.000 |
| **Soccer** | Team xG differential | Significantly more predictive than actual goal differential |
| **Golf** | Strokes gained tee-to-green | Course-fit models add incremental edge |
| **F1** | Qualifying pace | Tire degradation curves reveal hidden performance windows |
| **Tennis** | Surface-specific serve/return stats | Break point conversion is noisy; service games won is more stable |
| **Cricket** | Expected wickets, control % | Batting average is high-variance; strike rate context matters more |
| **Horse Racing** | Sectional timing (GPS) | Final time alone is misleading without pace/trip context |
| **MMA** | Significant strike differential | Striking accuracy + takedown defense combo is most predictive |

---

## Conclusion

The sports analytics data landscape in 2026 is defined by a paradox: tracking technology has never been more sophisticated, yet public access to raw data has arguably contracted. Soccer's FBref data loss, the NBA's tightening of API access, and horse racing's PDF fortress illustrate the trend.

### The Clearest Exceptions (Best Free Data)
1. **MLB's Baseball Savant** — Unmatched free pitch-level data
2. **nflfastR ecosystem** — 339 columns of open NFL data
3. **CricSheet** — Open ball-by-ball cricket data
4. **FastF1** — F1 telemetry that would cost millions in other contexts
5. **MoneyPuck** — 124-attribute shot data for 1.7M+ NHL shots

### The Practical Playbook for Modelers
1. **Use open-source libraries as primary data pipelines:** pybaseball, nba_api, nflfastR, FastF1, statsbombpy
2. **Supplement with mid-tier subscriptions:** DataGolf ($30/month), Evolving Hockey ($5/month), Cleaning the Glass ($7.50/month)
3. **Recognize the competitive moat:** Enterprise tracking data (Sportlogiq, Second Spectrum, Hawk-Eye raw feeds) remains what separates professional operations from public analysis

---

*Last updated: February 2026*
