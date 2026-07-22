# Red Letters

> *A comprehensive research project cataloging all known words and teachings of Jesus from canonical and extra-biblical sources*

## Project Vision

**Red Letters** aims to create the most complete, well-researched collection of Jesus's teachings available—stripping away layers of institutional interpretation to focus on the actual words attributed to him in historical sources.

### What This Project Is

- A **scholarly catalog** of Jesus's words from the canonical gospels ("red letter" text)
- A **comprehensive survey** of extra-biblical sources (Gnostic gospels, historical references, Islamic sources)
- A **chronological organization** of public speeches and private disciple teachings
- An **original language analysis** using Greek, Hebrew, and Aramaic sources
- A **cross-referencing system** connecting themes, contexts, and interpretations

### What This Project Is Not

- A theological statement or religious doctrine
- An attempt to prove or disprove religious claims
- A replacement for religious texts
- A promotion of any particular interpretation

## Repository Structure

```
red-letters/
├── docs/
│   ├── PROJECT-INDEX.md                          # Master index of all files
│   ├── JESUS-TEACHINGS-PROJECT.md                # Project methodology & guide
│   ├── JESUS-PUBLIC-SPEECHES-CHRONOLOGICAL.md    # 20 major public speeches
│   ├── JESUS-DISCIPLE-TEACHINGS-CHRONOLOGICAL.md # 40 private teachings
│   ├── EXTRA-BIBLICAL-JESUS-SOURCES.md           # Non-canonical sources catalog
│   └── bible-resources-research.md               # Technical infrastructure
├── data/
│   ├── canonical/          # Gospel sayings (Matthew, Mark, Luke, John)
│   ├── extra-biblical/     # Non-canonical sources
│   ├── analysis/           # Word studies, cross-references, commentaries
│   └── chronology/         # Timeline reconstructions
├── database/
│   └── schema/             # Database design for all teachings
├── scripts/
│   └── extraction/         # Automated extraction tools
└── .mcp.json               # MCP server configuration
```

## Current Status

### ✅ Completed (Phase 1 - Foundation)
- [x] MCP servers installed (studybible-mcp, TheologAI)
- [x] Infrastructure research (11 MCP servers, 9 APIs, 15 datasets cataloged)
- [x] Project methodology defined (6-phase research plan)
- [x] Chronological catalog: 20 major public speeches
- [x] Chronological catalog: 40 private disciple teachings
- [x] Extra-biblical sources: Nag Hammadi Library (7 gospels detailed)

### 🔄 In Progress (Phase 2 - Source Catalog)
- [ ] Complete extra-biblical sources catalog (Part 2):
  - Gospel of Peter, Judas, Infancy gospels
  - Papyrus fragments (Egerton, Oxyrhynchus)
  - Jewish sources (Josephus, Talmud)
  - Roman historians (Tacitus, Pliny, Suetonius)
  - Islamic sources (Quran, Hadith)
  - Early Church Fathers (Agrapha)

### 📋 To Do (Phase 3+ - Extraction & Analysis)
- [ ] Extract all canonical red letter text
- [ ] Greek/Hebrew/Aramaic text compilation
- [ ] Word studies and lexical analysis
- [ ] Cross-reference mapping
- [ ] Database implementation
- [ ] Commentary synthesis
- [ ] Extra-biblical text extraction

## Key Documents

### Getting Started
- **[PROJECT-INDEX.md](PROJECT-INDEX.md)** - Start here for complete overview
- **[JESUS-TEACHINGS-PROJECT.md](JESUS-TEACHINGS-PROJECT.md)** - Research methodology

### Chronological Catalogs
- **[JESUS-PUBLIC-SPEECHES-CHRONOLOGICAL.md](JESUS-PUBLIC-SPEECHES-CHRONOLOGICAL.md)** - 20 major public discourses
- **[JESUS-DISCIPLE-TEACHINGS-CHRONOLOGICAL.md](JESUS-DISCIPLE-TEACHINGS-CHRONOLOGICAL.md)** - 40 private teachings

### Source Research
- **[EXTRA-BIBLICAL-JESUS-SOURCES.md](EXTRA-BIBLICAL-JESUS-SOURCES.md)** - Non-canonical texts
- **[bible-resources-research.md](bible-resources-research.md)** - Technical tools & APIs

## Major Public Speeches (Sample)

| Event | Date | Location | Topic |
|-------|------|----------|-------|
| Sermon on the Mount | Spring 28 CE | Galilee | Beatitudes, Lord's Prayer, ethics |
| Bread of Life Discourse | Spring 29 CE | Capernaum | "I am the bread of life" |
| Olivet Discourse | March 31, 30 CE | Mount of Olives | End times, Second Coming |
| Upper Room Discourse | April 2, 30 CE | Jerusalem | Final teaching, Holy Spirit promise |

[See full chronological list →](JESUS-PUBLIC-SPEECHES-CHRONOLOGICAL.md)

## Extra-Biblical Sources (Sample)

| Source | Date | Content | Authenticity |
|--------|------|---------|--------------|
| Gospel of Thomas | 80-140 CE | 114 sayings | Moderate-High |
| Gospel of Philip | 180-250 CE | 15-17 sayings | Low |
| Josephus (Testimonium) | 93-94 CE | Historical mention | Debated |
| Quran | 609-632 CE | 25 surahs mention Isa | Islamic tradition |

[See full source catalog →](EXTRA-BIBLICAL-JESUS-SOURCES.md)

## Technical Infrastructure

This project uses:
- **MCP Servers:** studybible-mcp (18 tools), TheologAI (8 translations)
- **APIs:** GetBible API (100+ translations), ESV API, Bible Brain (audio)
- **Datasets:** scrollmapper/bible_databases (140 translations, MIT)
- **Tools:** Greek/Hebrew lexicons, morphological parsing, cross-references

[See technical details →](bible-resources-research.md)

## Research Methodology

### Six-Phase Approach

1. **Canonical Gospels** - Extract all red letter text from Matthew, Mark, Luke, John
2. **Acts & Epistles** - Post-resurrection words (Acts, Revelation)
3. **Original Languages** - Greek text, Hebrew/Aramaic reconstructions
4. **Cross-References** - Thematic connections, Old Testament fulfillment
5. **Commentaries** - Historical and modern scholarly interpretations
6. **Extra-Biblical** - Non-canonical sources (Gnostic gospels, Josephus, Quran, etc.)

[See full methodology →](JESUS-TEACHINGS-PROJECT.md)

## Database Schema

### Core Tables

**`jesus_sayings`** - Every recorded saying
- Scripture reference
- English, Greek, Aramaic text
- Context, audience, theme
- Canonical vs. extra-biblical
- Cross-references

**`word_studies`** - Linguistic analysis
- Greek/Hebrew words
- Strong's numbers
- Morphology, lexicon definitions
- Theological significance

**`commentaries`** - Historical interpretations
- Commentator name & tradition
- Commentary text
- Date & context

[See full schema →](JESUS-TEACHINGS-PROJECT.md#database-schema-proposed)

## How to Use This Research

### For Scholars
- Primary source citations with manuscript locations
- Original language texts with morphological parsing
- Cross-referenced with scholarly consensus dating

### For General Readers
- Chronological organization makes teachings easy to follow
- Plain English explanations of context
- Multiple translations for comparison

### For Software Developers
- Structured data suitable for apps/websites
- API access to bible text via MCPs
- Database schemas ready for implementation

## Contributing

This is an open research project. Contributions welcome:
- Additional source documentation
- Translation improvements
- Cross-reference identification
- Database implementations
- Extraction scripts
- Historical context research

## Installation (For Researchers)

### Prerequisites
- Claude Code CLI with MCP support
- Python 3.12+ (for studybible-mcp)
- Node.js 22+ (for TheologAI)

### Quick Start
```bash
# Clone repository
git clone https://github.com/chrissmithphd/red-letters.git
cd red-letters

# MCP servers are already configured in .mcp.json
# Restart Claude Code to load MCPs

# Test MCP connectivity
# In Claude: "Using studybible MCP, retrieve Matthew 5:1-12"
```

[See full installation guide →](JESUS-TEACHINGS-PROJECT.md#mcp-servers-installed)

## Data Sources

### Primary Sources
- **Canonical Gospels:** Matthew, Mark, Luke, John (Greek NT, ~50-100 CE)
- **Nag Hammadi Library:** 52 Gnostic texts discovered 1945 (~350 CE Coptic)
- **Papyrus Fragments:** Oxyrhynchus, Egerton (~200-300 CE)
- **Josephus:** Antiquities of the Jews (~93 CE)
- **Quran:** References to Isa (Jesus) (~650 CE)

### Translations & Tools
- 100+ Bible translations via GetBible API
- Strong's Concordance (14,298 entries)
- Greek lexicons (Liddell-Scott-Jones, Abbott-Smith)
- Hebrew lexicon (Brown-Driver-Briggs)

## Timeline

- **27-30 CE:** Jesus's public ministry (~3 years)
- **50-100 CE:** Canonical gospels written
- **100-250 CE:** Many Gnostic gospels composed
- **1945:** Nag Hammadi discovery
- **1947:** Dead Sea Scrolls discovery
- **2026:** Red Letters project initiated

## License

### Research & Documentation
All original research, documentation, and compilation: **CC BY-SA 4.0**
- Attribution required
- Share-alike required
- Commercial use allowed

### Ancient Texts
- Canonical scriptures: Public domain
- Nag Hammadi texts: Public domain (ancient texts)
- Modern translations: Various licenses (cited individually)

### Software & Data
- Database schemas: **MIT License**
- Extraction scripts: **MIT License**
- Structured data: **CC0 1.0** (public domain dedication)

## Project Name

**Red Letters** refers to the Christian publishing convention of printing Jesus's words in red ink in printed Bibles, making them stand out from narrative text. This project aims to collect, analyze, and present all those "red letter" words in their historical, linguistic, and cultural context.

## Scholarly Standards

This project follows:
- Peer-reviewed scholarly consensus for dating
- Primary source citations with manuscript locations
- Transparent methodology
- Multiple attestation principle
- Criterion of embarrassment
- Historical plausibility testing

## Acknowledgments

### Primary Resources
- **Nag Hammadi Scriptures** (HarperOne, 2007) - Marvin Meyer, ed.
- **The Historical Jesus** (HarperSanFrancisco, 1991) - John Dominic Crossan
- **Jesus: Apocalyptic Prophet** (Oxford, 1999) - Bart D. Ehrman
- **GetBible API** - Free bible text access
- **studybible-mcp** - Comprehensive bible study tools

### Contributors
- Project initiated by Chris Smith
- Research compiled using Claude Code + MCP servers
- Community contributions welcome

---

**Status:** Active Research Project  
**Started:** July 2026  
**Repository:** https://github.com/chrissmithphd/red-letters  
**Contact:** [Open an issue](https://github.com/chrissmithphd/red-letters/issues)

---

*"The words that I have spoken to you are spirit and life." - John 6:63*
