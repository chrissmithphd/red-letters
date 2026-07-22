# Jesus Teachings Research - Project Index

## File Organization

| File | Purpose | High-Level Topics |
|------|---------|-------------------|
| **bible-resources-research.md** | Technical infrastructure research | • MCP Servers (11 found)<br>• Bible APIs (9 evaluated)<br>• Datasets (15 repositories)<br>• Libraries & CLI Tools (30+)<br>• Installation guides<br>• Recommendations by use case |
| **JESUS-TEACHINGS-PROJECT.md** | Project methodology & guide | • MCP setup instructions<br>• Research phases (6 phases)<br>• How to use the MCPs<br>• Database schema proposals<br>• Sample workflows<br>• File structure recommendations<br>• Next steps checklist |
| **EXTRA-BIBLICAL-JESUS-SOURCES.md** | Non-canonical sources catalog | • Nag Hammadi Library texts<br>• Gnostic gospels (Thomas, Philip, Mary, etc.)<br>• Manuscript details & locations<br>• Jesus sayings counts<br>• Authenticity assessments<br>• Access information<br>• *[Part 2 coming: Jewish, Roman, Islamic sources]* |

---

## Detailed Topic Breakdown

### 📘 bible-resources-research.md
**Size:** ~920 lines | **Created:** July 9, 2026

**Section 1: MCP Servers (11 servers)**
- studybible-mcp (18 tools, most comprehensive)
- TheologAI (8 translations, 6 commentaries)
- FHL-MCP-Server (20+ translations, multilingual)
- LogosBibleSoftwareMCP
- bible-mcp, mcp-bible, lsbible
- translation-helps-mcp
- bible-study

**Section 2: Bible APIs (9 APIs)**
- GetBible API (100+ translations, free)
- API.Bible (commercial, licensed versions)
- ESV API (audio support)
- Bible-API.com (easiest to start)
- Bible Brain API (1,477 languages, audio)
- A Bíblia Digital API
- Others evaluated

**Section 3: Open Source Datasets (15 repositories)**
- scrollmapper/bible_databases (140 translations, MIT)
- HelloAOLab/bible-api (1,000+ translations)
- Clear-Bible/macula (scholarly Greek/Hebrew)
- BibleNLP/ebible (NLP research corpus)
- thiagobodruk/bible
- Others cataloged

**Section 4: Libraries & Tools (30+)**
- **CLI Tools:** christ-cli (Rust), bbl (Kotlin), bib (Shell), kjv (C), BibleMate (Python AI)
- **Python:** pythonbible, BibleOrgSys, pythonbible-parser
- **Node.js:** bibleapi-rest, bibleapi-graphql, usfm2json
- **Go:** bible-go-api
- **Rust:** usfm3
- **Ruby:** pericope
- **SWORD Project**

**Section 5: Recommendations by Use Case**
- Best for AI Integration (MCP)
- Best Free API
- Best for Commercial Projects
- Best for Terminal/CLI
- Best Python Library
- Best for Audio Bibles
- Best for NLP/Research
- Best Dataset
- Best for Quick Prototyping

**Section 6: Summary & Key Findings**
- Ecosystem overview (65+ resources)
- Key trends (MCP adoption, Rust dominance, Python ecosystem)
- Trade-offs summary
- Best practices
- Licensing considerations
- Community resources

---

### 📗 JESUS-TEACHINGS-PROJECT.md
**Size:** ~350 lines | **Created:** July 10, 2026

**Overview Section**
- Project goals and scope

**MCP Servers Installed**
1. studybible-mcp details (tools, capabilities, features)
2. TheologAI details (translations, commentaries, tools)

**Configuration**
- File locations
- How to restart Claude Code

**Research Methodology (6 Phases)**
1. **Phase 1:** Canonical Gospels (Matthew, Mark, Luke, John red letters)
2. **Phase 2:** Acts and Epistles (post-resurrection words)
3. **Phase 3:** Original Language Analysis (Greek, Hebrew, Aramaic)
4. **Phase 4:** Cross-References and Context
5. **Phase 5:** Commentaries and Interpretation
6. **Phase 6:** Extra-Biblical Sources (non-canonical texts)

**How to Use the MCPs**
- Example queries with MCP tool names
- Sample workflows for verse lookup, word studies, translations, commentaries

**Database Schema (Proposed)**
- `jesus_sayings` table structure
- `word_studies` table structure
- `commentaries` table structure

**Sample Workflow**
- Step-by-step extraction process
- From verse retrieval to database entry

**Additional Research Resources**
- APIs for later phases
- Datasets for offline work
- Extra-Biblical sources to research (Gospel of Thomas, Josephus, Quran, etc.)

**Next Steps**
- 7-step checklist from MCP testing to extra-biblical research

**Notes**
- Best practices and tips
- Thematic grouping suggestions

**File Structure (Proposed)**
- Directory tree for organizing research data

---

### 📙 EXTRA-BIBLICAL-JESUS-SOURCES.md
**Size:** ~550 lines (growing) | **Created:** July 10, 2026 | **Status:** Part 1 complete, Part 2 in progress

**Part 1: Nag Hammadi Library & Gnostic Gospels**

**Discovery Context**
- 1945 discovery details
- Manuscript dates and significance

**1. Gospel of Thomas** ⭐
- Manuscript details (Coptic + 3 Greek fragments)
- 114 sayings
- Notable quotes (Sayings 2, 77, 13, 114)
- Scholarly assessment
- Why excluded
- Access information

**2. Gospel of Philip**
- Valentinian Gnostic text
- 15-17 sayings
- Mary Magdalene "companion" passage
- Sacramental theology

**3. Gospel of Mary (Magdalene)**
- 3 manuscripts (Berlin Codex, P.Rylands, P.Oxy)
- Women's authority debate
- Peter vs. Levi conflict

**4. Gospel of Truth**
- Possibly by Valentinus
- Theological meditation (not sayings)

**5. Apocryphon of James**
- Post-resurrection dialogue
- 100-200 CE

**6. Apocryphon of John**
- 4 manuscripts
- Gnostic cosmology (Yaldabaoth demiurge)
- Sethian theology

**7. Dialogue of the Saviour**
- Possibly earliest core (1st century?)
- Mary Magdalene prominent

**Summary Table**
- All 7 gospels compared (date, sayings count, authenticity)

**Key Takeaways**
- Texts we actually have
- Highest authenticity potential
- Where to access

**Part 2: [In Progress]**
- Other apocryphal gospels (Peter, Judas, Infancy)
- Papyrus fragments (Egerton, Oxyrhynchus)
- Jewish sources (Josephus, Talmud, Toledot Yeshu)
- Roman/Greek historians (Tacitus, Pliny, Suetonius, Lucian)
- Islamic sources (Quran, Hadith)
- Early Church Fathers (Agrapha - unwritten sayings)
- Apocryphal Acts (Thomas, Peter, John)

---

## Quick Reference: What's Where?

### Need to know HOW to access bible text?
→ **bible-resources-research.md**

### Need to know HOW to do the research project?
→ **JESUS-TEACHINGS-PROJECT.md**

### Need to know WHAT extra-biblical sources exist?
→ **EXTRA-BIBLICAL-JESUS-SOURCES.md**

---

## Configuration Files

| File | Purpose |
|------|---------|
| `.mcp.json` | MCP server configuration for Claude Code CLI |

---

## Current Status

✅ **Complete:**
- MCP servers installed (studybible-mcp, TheologAI)
- Technical infrastructure research
- Project methodology defined
- Nag Hammadi gospels cataloged

⏳ **In Progress:**
- Extra-biblical sources Part 2 (Jewish, Roman, Islamic sources)

🔲 **To Do:**
- Restart Claude Code to load MCPs
- Test MCP connectivity
- Begin canonical gospel extraction
- Set up database
- Build extraction scripts

---

*Last Updated: July 10, 2026*
