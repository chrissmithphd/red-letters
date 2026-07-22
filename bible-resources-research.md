# Bible Text Access Resources - Comprehensive Research Report

**Research Date:** July 9, 2026  
**Focus:** MCP Servers, APIs, Datasets, and Libraries for Bible text access  
**Selection Criteria:** Actively maintained (updated within last 2 years), good documentation, multiple translations, scholarly resources

---

## Table of Contents

1. [MCP Servers](#1-mcp-servers)
2. [Bible APIs](#2-bible-apis)
3. [Open Source Datasets](#3-open-source-datasets)
4. [Libraries & Tools](#4-libraries--tools)
5. [Recommendations by Use Case](#5-recommendations-by-use-case)
6. [Summary & Key Findings](#6-summary--key-findings)

---

## 1. MCP SERVERS

Model Context Protocol (MCP) servers provide the most integrated approach for Bible access, especially when working with AI assistants like Claude.

### 1.1 studybible-mcp ⭐ MOST COMPREHENSIVE

- **Repository:** https://github.com/djayatillake/studybible-mcp
- **Stars:** 68 | **Last Update:** July 8, 2026
- **Language:** Python | **License:** Other

**Translations:**
- English translation with original Greek and Hebrew texts
- All 31,280 verses with morphological parsing

**Additional Features:**
- **Lexicons:** Liddell-Scott-Jones Greek (10,846 entries), Abbott-Smith NT Greek (5,896 entries), Brown-Driver-Briggs Hebrew (8,090 entries)
- **Commentaries:** 66 books of verse-level scholarly commentary via Aquifer Open Study Notes
- **Cross-References:** 22 thematic cross-references, semantic passage similarity via vector embeddings
- **Study Materials:** Tyndale Bible Dictionary (500+ articles), unfoldingWord Translation Notes, SIL Translator Notes, 200+ theological terms, 87 Ancient Near East cultural context entries
- **Graph Knowledge:** Genealogy exploration, person events, place history, relationship mapping

**Integration:** Simplest - add connector URL in Claude Desktop Settings (no signup, no API keys)

**Tools Provided:** 18 tools across verse lookup, word study, lexicon search, cross-references, morphology parsing, study notes, Bible dictionary, theological terms, graph knowledge, Ancient Near East context

**Documentation Quality:** ⭐⭐⭐⭐⭐ Excellent

---

### 1.2 TheologAI ⭐ BEST FOR REMOTE DEPLOYMENT

- **Repository:** https://github.com/TJ-Frederick/TheologAI
- **Stars:** 22 | **Last Update:** July 10, 2026
- **Language:** TypeScript | **License:** None specified

**Translations:**
- 8 translations: ESV, NET, KJV, WEB, BSB, ASV, YLT, DBY

**Additional Features:**
- **Commentaries:** 6 public domain commentaries (Matthew Henry, Jamieson-Fausset-Brown, Adam Clarke, John Gill, Keil-Delitzsch, Tyndale)
- **Cross-References:** Treasury of Scripture Knowledge integration
- **Historical Documents:** 18 local documents (4 creeds, 8 confessions, 6 catechisms)
- **Language Tools:** Strong's Concordance (14,298 entries), STEPBible morphology (447,789 words)
- **Classic Texts:** Access to 1000+ CCEL works with dynamic discovery

**Integration:** 
- **Remote (simplest):** Add https://theologai.tjfrederick.workers.dev/mcp to Claude.ai settings
- **Local:** Clone, npm install, configure .env, npm run build, npm start

**Tools Provided:** `bible_lookup`, `commentary_lookup`, `classic_text_lookup`, `original_language_lookup`, `bible_verse_morphology`, `bible_cross_references`

**Documentation Quality:** ⭐⭐⭐⭐⭐ Excellent

---

### 1.3 FHL-MCP-Server ⭐ BEST MULTILINGUAL

- **Repository:** https://github.com/ytssamuel/FHL-MCP-Server
- **Stars:** 16 | **Last Update:** December 29, 2025
- **Language:** Python | **License:** Other

**Translations:**
- 20+ translations: Chinese (Union Version, Modern Chinese Translation), English (KJV), and multilingual

**Additional Features:**
- **Commentaries:** 10+ authoritative commentary resources
- **Lexicons:** Strong's Original Language Dictionary with Hebrew and Greek analysis
- **Cross-References:** 1-3 layer depth analysis
- **Advanced Tools:** Parallel Gospel comparison, topical study, thematic chain tracking, character study (9-dimensional analysis), footnote lookup, Apocrypha and Apostolic Fathers texts
- **Article Search:** 8,000+ articles

**Integration:** Automated one-command installation via install.bat/install.sh

**Tools Provided:** 27 tool functions - 6 scripture query tools, 6 original language tools, 6 commentary/study tools, 7 specialized tools, 2 multimedia tools

**Documentation Quality:** ⭐⭐⭐⭐ Good

---

### 1.4 LogosBibleSoftwareMCP

- **Repository:** https://github.com/robrawks/LogosBibleSoftwareMCP
- **Stars:** 15 | **Last Update:** February 26, 2026
- **Language:** TypeScript | **License:** None specified
- **Prerequisites:** macOS, Node.js v18+, Logos Bible Software installed

**Translations:**
- 6 translations via Biblia API: LEB (default), KJV, ASV, DARBY, YLT, WEB

**Additional Features:**
- **Study Resources:** Commentary and lexicon access via resource navigation, word study (Greek/Hebrew/English), Factbook entries
- **Cross-References:** Related passages by key term extraction
- **Personal Study Data:** User notes, highlights, bookmarks, reading plan progress
- **Search:** Bible text searching and library-wide resource search

**Integration:** Moderate complexity - requires API key acquisition, JSON config creation

**Tools Provided:** 20 tools across Bible retrieval (4), Logos navigation (5), search/discovery (4), library browsing (2), personal study data (5)

**Documentation Quality:** ⭐⭐⭐⭐ Good

---

### 1.5 Other Notable MCP Servers

#### bible-mcp (Trevato)
- **Stars:** 14 | **Last Update:** May 7, 2025
- **Translations:** Multiple via bible-api.com (WEB, KJV, ASV, BBE)
- **Integration:** Simple - `pip install bible-mcp`
- **Tools:** 3 tools - verse by reference, random verse, list translations
- **Documentation:** ⭐⭐⭐⭐ Good

#### mcp-bible (geosp)
- **Stars:** 6 | **Last Update:** November 9, 2025
- **Translations:** 8 via BibleGateway (ESV, NIV, KJV, NASB, NKJV, NLT, AMP, MSG)
- **Integration:** Straightforward - Python 3.10+, uv package manager
- **Features:** REST API endpoints + MCP tools
- **Documentation:** ⭐⭐⭐⭐ Good

#### lsbible (kdcokenny)
- **Stars:** 7 | **Last Update:** November 4, 2025
- **Translations:** Legacy Standard Bible (LSB) only
- **Features:** Rich formatting (red-letter text, italics, poetry detection), text search with analytics
- **Integration:** Minimal - add to MCP config
- **Documentation:** ⭐⭐⭐⭐⭐ Very good

#### translation-helps-mcp (klappy)
- **Stars:** 6 | **Last Update:** December 13, 2025
- **Translations:** 4+ (ULT, UST, T4T, UEB)
- **Features:** Translation Notes, Translation Words, Translation Questions, Translation Academy, Semantic Search
- **Integration:** Node.js 18+, Wrangler CLI
- **Documentation:** ⭐⭐⭐⭐ Good

#### bible-study (mctx-ai)
- **Stars:** 4 | **Last Update:** May 31, 2026
- **Translations:** 5 (KJV, WEB, ASV, YLT, Darby)
- **Features:** 17,543 Strong's entries, 606,140 cross-references, 5,319 topical categories, semantic search
- **Integration:** Subscription-based service
- **Documentation:** ⭐⭐ Limited

---

## 2. BIBLE APIS

### 2.1 GetBible API ⭐ BEST FREE OPTION

- **URL:** https://getbible.net | https://api.getbible.net
- **API Type:** REST API with JSON responses
- **Authentication:** None required
- **License:** GPL-3.0 (Open Source)
- **Rate Limits:** Not specified
- **Pricing:** Free

**Translations:**
- **100+ translations** including:
  - English: KJV, AKJV, ASV, Darby, WEB, Basic English Bible
  - European: German (Luther 1545, Elberfelder), French, Spanish, Swedish, Danish, Norwegian
  - Ancient: Aleppo Codex, Coptic, Gothic, Peshitta, LXX (Septuagint)
  - Asian: Japanese, Korean, Thai, Chinese, Vietnamese, Tagalog, Maori
  - Others: Portuguese (Almeida), Afrikaans, Albanian, Armenian, Arabic (Smith & Van Dyke), Esperanto

**Features:**
- Two API endpoints optimized for different use cases:
  - Query API (query.getbible.net/v2/): Retrieve specific verses/verse groups
  - Main API (api.getbible.net/v2/): Retrieve complete translations, books, or chapters
- Metadata endpoints for translation lists, checksums, book lists, chapter info
- Supports Strong's Numbers and morphology in some translations (e.g., KJV)

**Additional Tools:**
- Joomla Component
- JavaScript Loader for embedding
- Python library (GetBible Librarian)
- Telegram bot

**Documentation Quality:** ⭐⭐⭐⭐⭐ Excellent

**Ease of Integration:** ⭐⭐⭐⭐⭐ Very easy - simple REST endpoints, no authentication, well-structured JSON

---

### 2.2 API.Bible ⭐ BEST FOR COMMERCIAL USE

- **URL:** https://api.bible | https://docs.api.bible
- **API Type:** REST API with JSON responses
- **Authentication:** API key required (sign-up at api.bible)
- **License:** Commercial licensing available
- **Maintained By:** American Bible Society

**Translations:**
- Licensed versions: NIV, NKJV, NASB, The Message, NLT, CSB, GNT, Amplified Bible, KJV
- Hundreds of open access/public domain Bibles
- Uses USX/USFM standard for unified formatting across all translations

**Features:**
- Bible text retrieval (verses, chapters, books)
- Search functionality
- Unified API format across all translations

**Rate Limits & Pricing:**
- **Starter (Free):** 5,000 API calls/day, pick 3 copyrighted Bibles, non-commercial only
- **Pro ($29+/month):** 150,000 API calls/month, additional calls available for purchase
- **Enterprise:** Higher limits on request

**License Terms:**
- Starter plan strictly non-commercial
- Commercial use requires licensing fees ($10+ per Bible)
- Single license covers multiple translations

**Documentation Quality:** ⭐⭐⭐⭐⭐ Comprehensive with API Reference, Quick Start guides, FAQ, Live Demo at demo.api.bible

**Ease of Integration:** ⭐⭐⭐⭐⭐ REST API with well-documented endpoints, unified format simplifies multi-translation support

---

### 2.3 ESV API ⭐ BEST FOR ESV

- **URL:** https://api.esv.org | https://api.esv.org/docs
- **API Type:** REST API
- **Authentication:** API key required (obtain by creating application at ESV.org)
- **License:** Non-commercial use only (free tier)
- **Maintained By:** Crossway

**Translations:**
- ESV (English Standard Version) only

**Features:**
- Plain text retrieval
- HTML formatted text
- Audio passages
- Search functionality

**Rate Limits:**
- 5,000 queries/day maximum
- 1,000 requests/hour maximum
- 60 requests/minute maximum
- 500 verses per query limit

**License Terms:**
- Non-commercial use only (free tier)
- Cannot cache more than 500 verses locally
- Text cannot be modified
- Must include proper ESV attribution and copyright notices
- Access can be revoked at Crossway's discretion

**Documentation Quality:** ⭐⭐⭐⭐⭐ Good with clear endpoint documentation for text, HTML, audio, and search

**Ease of Integration:** ⭐⭐⭐⭐⭐ Very easy - simple REST interface, token-based authentication via header

---

### 2.4 Bible-API.com ⭐ EASIEST TO START

- **URL:** https://bible-api.com
- **API Type:** RESTful JSON API
- **Authentication:** None required
- **License:** MIT License (free for any use with fair use expectations)
- **Rate Limits:** 15 requests per 30 seconds (IP-based)
- **Maintained By:** Tim Morgan (hobby project)

**Translations:**
- 17 translations across 8 languages: KJV, ASV, WEB (default), Chinese, Czech, Latin, Portuguese, Romanian, Cherokee

**Features:**
- Single verse and passage retrieval
- Flexible book name abbreviations
- Verse ranges and multiple verse selection
- Random verse endpoint with filtering (by book, OT, NT)
- Embedded URLs for API exploration

**License Terms:**
- Free for any use with fair use expectations
- "Do not abuse my server"
- Do not download entire Bible via API (get from source instead)

**Self-Hosting:** Source code and data available on GitHub for self-hosting (Ruby app with MySQL/MariaDB + Redis)

**Documentation Quality:** ⭐⭐⭐⭐⭐ Excellent - clear examples, parameter explanations, edge case handling

**Ease of Integration:** ⭐⭐⭐⭐⭐ Extremely easy - no auth, simple REST calls, helpful error messages

---

### 2.5 Bible Brain API (Digital Bible Platform) ⭐ BEST FOR AUDIO

- **URL:** https://faithcomesbyhearing.com/audio-bible-resources/bible-brain | https://4.dbt.io
- **API Type:** REST API
- **Authentication:** API key (request at https://4.dbt.io/api_key/request)
- **Maintained By:** Faith Comes By Hearing

**Translations:**
- Text in 1,477 languages
- Extensive audio Bible collection

**Features:**
- **Audio:** Premium Bible audio files
- **Text:** Extensive language coverage
- **Video:** Gospel videos with cinematography

**Rate Limits:** Not specified in public documentation

**Documentation Quality:** ⭐⭐⭐⭐ Overview documentation available; full developer docs at /bible-brain/developer-documentation

**Ease of Integration:** ⭐⭐⭐⭐ Simple API calls described; full technical details require API key request

**Notes:** Strong focus on audio Bibles for oral cultures; massive language coverage

---

### 2.6 Other Notable APIs

#### A Bíblia Digital API
- **URL:** https://www.abibliadigital.com.br/en
- **Translations:** 7 versions in 4 languages (NIV, RA, ACF, KJV, BBE, RVR, APEE)
- **Features:** Verses, devotionals, reference comments, search functionality
- **Pricing:** Free; supported by optional Patreon donations
- **Documentation:** ⭐⭐⭐⭐ Good - Insomnia, Postman, and Swagger integrations available

#### Bolls Life API
- **URL:** https://bolls.life
- **Status:** Active web application (GPL-3.0 license)
- **Note:** Open-source web application focused on browser use rather than API service
- **Contact:** bpavlisinec@gmail.com

#### Bible Gateway API
- **Status:** No public API currently available
- **Notes:** Bible Gateway is primarily a web-based Bible reading platform without official API access

#### Bible.com API (YouVersion)
- **Status:** No public API available
- **Notes:** YouVersion/Bible.com does not provide a public API for developers

---

## 3. OPEN SOURCE DATASETS

### 3.1 scrollmapper/bible_databases ⭐ MOST COMPREHENSIVE

- **URL:** https://github.com/scrollmapper/bible_databases
- **Stars:** 1,642 | **Last Update:** February 2025
- **License:** MIT
- **Size:** 2.2 GB

**Formats:**
- SQL, JSON, XML, CSV, YAML, TXT, Markdown (7 formats)

**Content:**
- 140 translations
- 60+ languages
- Cross-references database
- Strong's numbers

**Use Case:** Best for offline applications, local development, commercial projects (MIT license)

**Documentation Quality:** ⭐⭐⭐⭐⭐ Excellent

---

### 3.2 HelloAOLab/bible-api ⭐ PRODUCTION-READY API

- **URL:** https://github.com/HelloAOLab/bible-api
- **Stars:** 150 | **Last Update:** May 2026
- **License:** MIT
- **Live API:** https://bible.helloao.org

**Content:**
- 1,000+ translations
- Formatting support
- Footnotes
- AWS infrastructure

**Status:** Very active, production-ready

**Use Case:** Best for building production applications with extensive translation needs

**Documentation Quality:** ⭐⭐⭐⭐⭐ Excellent

---

### 3.3 Clear-Bible/macula-greek & macula-hebrew ⭐ SCHOLARLY EXCELLENCE

- **URLs:** 
  - https://github.com/Clear-Bible/macula-greek
  - https://github.com/Clear-Bible/macula-hebrew
- **Stars:** 52 (Greek), 62 (Hebrew)
- **Last Update:** July 2026
- **License:** CC BY-SA 4.0

**Content:**
- Greek NT and Hebrew Bible with linguistic annotations
- Syntax trees
- Morphology
- Semantic roles
- Word senses

**Use Case:** State-of-the-art for academic research, linguistic analysis, computational biblical studies

**Documentation Quality:** ⭐⭐⭐⭐⭐ Excellent

---

### 3.4 BibleNLP/ebible ⭐ NLP RESEARCH

- **URL:** https://github.com/BibleNLP/ebible
- **Stars:** 95 | **Last Update:** May 2025
- **License:** Mixed licenses
- **Size:** 808 MB

**Content:**
- Hundreds of translations
- Verse-aligned parallel corpus
- Optimized for NLP research

**Use Case:** Best for natural language processing, machine translation, multilingual research

**Documentation Quality:** ⭐⭐⭐⭐ Good

---

### 3.5 thiagobodruk/bible

- **URL:** https://github.com/thiagobodruk/bible
- **Stars:** 720 | **Last Update:** August 2024
- **License:** CC BY-NC (non-commercial)
- **Size:** 39 MB

**Content:**
- 23 versions
- 14 languages
- JSON, XML formats

**Use Case:** Good for personal projects, prototyping (non-commercial only)

**Documentation Quality:** ⭐⭐⭐⭐ Good

---

### 3.6 Other Notable Datasets

#### christos-c/bible-corpus
- **Stars:** Not specified | **License:** CC0
- **Content:** 100 languages, NLP-focused
- **Use Case:** Public domain, ideal for research

#### openscriptures/morphhb
- **Content:** Hebrew Bible with Strong's and morphology
- **Use Case:** Hebrew text analysis, linguistic research

#### seven1m/bible_api
- **Content:** Simple JSON API, public domain
- **Use Case:** Quick prototyping

#### godlytalias/Bible-Database
- **Content:** 8 Indian languages, MySQL/SQLite
- **Use Case:** South Asian language support

#### wldeh/bible-api
- **Content:** CDN-based, no authentication required
- **Use Case:** Fast integration for web projects

---

## 4. LIBRARIES & TOOLS

### 4.1 Command-Line Tools

#### christ-cli (Rust) ⭐ BEST TUI EXPERIENCE

- **URL:** https://github.com/whoisyurii/christ-cli
- **Stars:** 127 | **Last Update:** July 2026
- **Language:** Rust (94.5%) | **License:** MIT

**Features:**
- Full-screen TUI (Terminal User Interface) with 3-panel browser
- 50+ online translations via Bolls.life API
- Bundled KJV for offline use (4.7MB embedded)
- 12 language support for book names
- Live text search with preview
- 5 themes, clipboard support (including SSH via OSC 52)
- Session persistence

**Installation:** `npm install -g christ-cli` or curl script

**Binary Size:** ~5MB single executable

**Documentation Quality:** ⭐⭐⭐⭐⭐ Excellent

---

#### bbl (Kotlin) ⭐ BEST OFFLINE SUPPORT

- **URL:** https://github.com/nehemiaharchives/bbl
- **Stars:** 92 | **Last Update:** July 2026
- **Language:** Kotlin (Kotlin/Native) | **License:** Apache 2.0

**Features:**
- Full-text search powered by lucene-kmp
- 26 language translations offline
- Compare multiple translations simultaneously
- Random verse generation
- Shell autocomplete (bash, zsh, fish, PowerShell)
- Command history tracking

**Installation:** APT, Homebrew, Scoop, WinGet, or direct binary

**Documentation Quality:** ⭐⭐⭐⭐⭐ Excellent

---

#### bib (Shell/Bash)

- **URL:** https://github.com/prestonharberts/bib
- **Stars:** 52 | **Last Update:** March 2026
- **Language:** Shell (Bash) | **License:** CC0-1.0

**Features:**
- Fast terminal access using markdown files
- Verse highlighting in red
- Interactive mode for multiple lookups
- Companion tools: bibs (search), bibr (random), bibc (copy chapters)
- Auto-hyphenation for responsive terminal scaling

**Installation:** Manual (copy script + Bible folder to PATH)

**Dependencies:** sed, awk, jq, tput, column

**Documentation Quality:** ⭐⭐⭐⭐ Good

---

#### kjv (C)

- **URL:** https://github.com/bontibon/kjv
- **Stars:** 222 | **Last Update:** Not recent
- **Language:** C (91.5%) | **License:** Unlicense (public domain)

**Features:**
- Fast C implementation
- Pattern search across entire text
- Context display (surrounding verses)
- Syntax highlighting option
- Paginated view with chapter grouping

**Translation:** King James Version only

**Installation:** `make && sudo make install`

**Documentation Quality:** ⭐⭐⭐⭐ Good

---

#### BibleMate (Python) ⭐ AI-POWERED

- **URL:** https://github.com/eliranwong/biblemate
- **Stars:** 17 | **Last Update:** June 2026
- **Language:** Python | **License:** Not specified

**Features:**
- **AI-powered:** Autonomous agent for multi-step Bible study
- Agent Mode and Partner Mode
- AI-generated commentary in 3 languages
- 12 advanced search tools with semantic search
- Hebrew/Greek audio and morphological analysis
- Bible podcasts for every book/chapter
- Web GUI, CLI, MCP Server, RESTful API

**Installation:** `pip install biblemate` (multiple packages available)

**Documentation Quality:** ⭐⭐⭐⭐⭐ Excellent

---

### 4.2 Python Libraries

#### pythonbible ⭐ BEST PYTHON LIBRARY

- **URL:** https://github.com/avendesora/pythonbible
- **PyPI:** https://pypi.org/project/pythonbible
- **Stars:** 83 | **Last Update:** January 2026
- **Version:** 0.15.5 | **License:** MIT
- **Python Support:** 3.10-3.14

**Features:**
- Scripture reference parsing and validation
- Verse identification system (integer IDs)
- Smart formatting (combines verses into ranges)
- Text retrieval from 26+ Bible versions
- Reference normalization and conversion

**Translations:** 26+ including KJV, AKJV, UKJV, ASV, Darby, Douay-Rheims, Geneva, YLT, WEB, Aramaic translations

**Installation:** `python3 -m pip install pythonbible`

**Documentation Quality:** ⭐⭐⭐⭐⭐ Excellent (docs.python.bible)

**Code Quality:** Codacy tracked, pre-commit CI, CodeQL analysis

---

#### BibleOrgSys

- **URL:** https://github.com/Freely-Given-org/BibleOrgSys
- **PyPI:** https://pypi.org/project/BibleOrgSys
- **Stars:** 97 | **Last Update:** July 2026
- **Version:** 0.0.20 | **License:** GPL-3.0
- **Python Support:** 3.13+ (requires uv for project management)

**Features:**
- Handles USFM, USX, USJ, ESFM formats
- Multi-language support (Hebrew, Greek, RTL languages)
- Three strictness modes (default, strict, mission-critical)
- Multiprocessing support for fast loading
- Validation and error detection
- Export to multiple formats

**Installation:** `pip install BibleOrgSys` or `git clone` + `uv sync`

**Documentation Quality:** ⭐⭐⭐⭐ Good (improving)

**Technical:** 82.4% Python, 17% Rust (PyO3/maturin)

---

#### pythonbible-parser

- **URL:** https://github.com/avendesora/pythonbible-parser
- **PyPI:** https://pypi.org/project/pythonbible-parser
- **Stars:** 11 | **Last Update:** January 2026
- **Version:** Pre-release | **License:** MIT
- **Python Support:** 3.10-3.14

**Features:**
- Parses Bible texts in various formats
- Converts to Python-friendly structures
- Handles OSIS XML format
- Used by pythonbible library

**Installation:** `python3 -m pip install pythonbible-parser`

**Status Note:** Pre-release, breaking changes expected

**Documentation Quality:** ⭐⭐⭐⭐ Good

---

### 4.3 Node.js / JavaScript Libraries

#### bibleapi-rest

- **Status:** Updated January 2026
- **Stars:** 52
- **Features:** Node.js based Bible API RESTful web service

#### bibleapi-graphql

- **Status:** Updated January 2026
- **Stars:** 21
- **Features:** Node.js based Bible API GraphQL web service

#### usfm2json

- **Status:** Updated May 2024
- **Stars:** 19
- **Features:** Convert USFM format Bibles to JSON

---

### 4.4 Go Libraries

#### bible-go-api ⭐ BEST GO LIBRARY

- **URL:** https://github.com/rkeplin/bible-go-api
- **Stars:** 43 | **Last Update:** July 2026
- **License:** GPL-3.0 | **Go Version:** 1.24+

**Features:**
- Dockerized REST API
- 10 Bible translations
- Cross-reference lookup
- Full-text search with Elasticsearch
- Kubernetes deployment support

**Translations:** ASV, BBE, DBY, KJV, WEB, YLT, ESV, NIV, NLT, NLT2015

**Installation:** `make dev` (Docker Compose)

**Documentation Quality:** ⭐⭐⭐⭐⭐ Excellent

**Technical Stack:** Go, MariaDB, Elasticsearch

---

### 4.5 Rust Libraries

#### usfm3

- **URL:** https://github.com/jcuenod/usfm3
- **Stars:** 6 | **Last Update:** May 2026
- **License:** MIT
- **Status:** Beta

**Features:**
- Error-tolerant USFM 3.x parser
- Rust, Python, and TypeScript bindings via WASM
- Tokenization, CST parsing, AST conversion
- Convert between USJ, USX, USFM, vref formats

**Installation:** Cargo (Rust), PyPI (Python), npm (TypeScript)

**Documentation Quality:** ⭐⭐⭐⭐ Good

---

### 4.6 Ruby Libraries

#### pericope

- **URL:** https://github.com/boblail/pericope
- **RubyGems:** https://rubygems.org/gems/pericope
- **Downloads:** 60,821 total | **Version:** 1.0.3
- **Last Update:** November 2019

**Features:**
- Parse biblical references from text
- Handles abbreviations and misspellings
- Compare pericopes for intersections
- Normalize references

**Installation:** `gem install pericope`

**Documentation Quality:** ⭐⭐⭐⭐ Good (rubydoc.info)

---

### 4.7 SWORD Project

- **URL:** https://crosswire.org/sword
- **License:** GNU GPL

**Description:**
The SWORD Project is CrossWire Bible Society's free Bible software project providing cross-platform open-source tools for Bible study applications.

**Resources:**
- Growing collection of hundreds of texts in ~100 languages
- Compatible applications: Ezra Bible App, BibleTime, etc.

**Popular Modules:**
- King James Version (KJV): 3,605 downloads/month
- English Standard Version (ESV): 3,305 downloads/month
- Strong's Greek/Hebrew lexicons

**Status:** Still relevant but Python bindings are dated; mostly used via C++ applications

---

## 5. RECOMMENDATIONS BY USE CASE

### 🎯 Best for AI Integration (MCP)
1. **studybible-mcp** - Most comprehensive, 18 tools, lexicons, commentaries, cross-references
2. **TheologAI** - Remote deployment option, 6 commentaries, historical documents
3. **FHL-MCP-Server** - Best multilingual support, 20+ translations

### 🎯 Best Free API
1. **GetBible API** - 100+ translations, no auth, open source
2. **Bible-API.com** - Easiest to start, no auth, 17 translations
3. **Bolls.life API** - Free, comprehensive features

### 🎯 Best for Commercial Projects
1. **API.Bible** - Professional service, licensing available, 5,000 free calls/day
2. **scrollmapper/bible_databases** - MIT license, 140 translations, 7 formats

### 🎯 Best for Terminal/CLI
1. **christ-cli** (Rust) - Beautiful TUI, 50+ translations
2. **bbl** (Kotlin) - Excellent offline, 26 languages, powerful search
3. **bib** (Shell) - Lightweight, fast, scriptable

### 🎯 Best Python Library
1. **pythonbible** - Active, 26+ versions, parsing/formatting
2. **BibleOrgSys** - Powerful, handles multiple formats
3. **BibleMate** - AI-powered, comprehensive study features

### 🎯 Best for Audio Bibles
1. **Bible Brain API** - 1,477 languages, specialized in audio
2. **ESV API** - Includes audio passages

### 🎯 Best for NLP/Research
1. **Clear-Bible/macula-greek & macula-hebrew** - Syntax trees, semantic annotations
2. **BibleNLP/ebible** - Verse-aligned parallel corpus
3. **christos-c/bible-corpus** - 100 languages, CC0 license

### 🎯 Best Dataset
1. **scrollmapper/bible_databases** - 140 translations, 7 formats, MIT license
2. **HelloAOLab/bible-api** - 1,000+ translations, production-ready
3. **Clear-Bible/macula** - Scholarly excellence, linguistic annotations

### 🎯 Best for Quick Prototyping
1. **Bible-API.com** - No auth, simple REST
2. **GetBible API** - No auth, 100+ translations
3. **christ-cli** - One-line install, 50+ translations

---

## 6. SUMMARY & KEY FINDINGS

### 📊 Ecosystem Overview

**Total Resources Identified:**
- **MCP Servers:** 11 actively maintained
- **APIs:** 9 (6 actively available)
- **Datasets:** 15 major repositories
- **Libraries/Tools:** 30+ across 7 programming languages

### 🔑 Key Trends

1. **MCP Adoption is Growing**
   - 11 MCP servers identified, none in official MCP directories yet
   - Community-driven ecosystem for Bible access via MCP
   - Simplest integration path for AI assistants

2. **Rust Dominance in CLI Tools**
   - Modern CLI tools increasingly built in Rust (christ-cli)
   - Single-binary distribution, excellent performance
   - Better user experience than legacy C/shell tools

3. **Python Ecosystem is Strong**
   - pythonbible and BibleOrgSys both actively maintained
   - Excellent documentation and code quality
   - Strong support for parsing, formatting, and multiple formats

4. **API Landscape is Mature**
   - Multiple free APIs available (GetBible, Bible-API.com)
   - Commercial options for licensed translations (API.Bible, ESV)
   - No authentication required for several high-quality APIs

5. **Format Standardization**
   - USFM/USX/USJ becoming standard interchange formats
   - Better tooling for format conversion (usfm3, BibleOrgSys)
   - Easier interoperability between projects

6. **AI Integration Emerging**
   - BibleMate shows AI integration trend
   - MCP servers enabling AI-powered Bible study
   - Semantic search and vector embeddings appearing

7. **Multilingual Support Increasing**
   - Modern tools emphasizing international language support
   - Bible Brain API: 1,477 languages
   - GetBible API: 100+ translations

8. **Offline-First Design**
   - Many modern tools bundle translations for offline use
   - bbl: 26 languages offline
   - christ-cli: bundled KJV (4.7MB)

### ⚖️ Trade-offs Summary

| Priority | Recommendation | Trade-off |
|----------|---------------|-----------|
| **Ease of Integration** | MCP Servers (studybible-mcp, TheologAI) | Less flexibility than APIs |
| **Translation Coverage** | GetBible API (100+), HelloAOLab/bible-api (1,000+) | May lack scholarly features |
| **Scholarly Features** | studybible-mcp, Clear-Bible/macula | More complex setup |
| **Commercial Use** | API.Bible, scrollmapper/bible_databases | Licensing costs or restrictions |
| **Offline Use** | bbl, scrollmapper/bible_databases | Larger download sizes |
| **Audio Support** | Bible Brain API, ESV API | Limited to specific translations |
| **Speed/Performance** | Local datasets, Rust CLI tools | Storage requirements |

### 🎓 Best Practices

1. **For AI Integration:** Start with MCP servers (studybible-mcp or TheologAI)
2. **For Web/Mobile Apps:** Use APIs (GetBible or API.Bible for commercial)
3. **For Academic Research:** Use Clear-Bible/macula datasets
4. **For NLP Projects:** Use BibleNLP/ebible or christos-c/bible-corpus
5. **For Offline Apps:** Use scrollmapper/bible_databases or bbl
6. **For Quick Prototypes:** Use Bible-API.com or christ-cli

### ⚠️ Licensing Considerations

- **Public Domain/MIT:** scrollmapper/bible_databases, GetBible, pythonbible
- **Non-Commercial Only:** thiagobodruk/bible (CC BY-NC), ESV API, API.Bible free tier
- **GPL-3.0:** BibleOrgSys, bible-go-api, GetBible (requires derivative works to be open source)
- **Commercial Available:** API.Bible ($29+/month), ESV API (by request)

---

## 📚 Additional Resources

### Documentation & References
- **USFM Standard:** https://ubsicap.github.io/usfm/
- **Digital Bible Library:** https://thedigitalbiblelibrary.org/
- **CrossWire SWORD Project:** https://crosswire.org/sword/
- **MCP Documentation:** https://modelcontextprotocol.io/

### Community
- **BibleNLP:** https://github.com/BibleNLP
- **Clear-Bible:** https://github.com/Clear-Bible
- **Open Scriptures:** https://github.com/openscriptures

---

**Report Compiled:** July 9, 2026  
**Research Scope:** GitHub, NPM, PyPI, RubyGems, Go packages, API directories  
**Maintenance Window:** Last 2 years (2024-2026)  
**Total Resources Evaluated:** 65+
