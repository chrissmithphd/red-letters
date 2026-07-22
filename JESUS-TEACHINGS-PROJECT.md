# Jesus Teachings Research Project

## Overview
A comprehensive chronicle of all known words and teachings of Jesus, including canonical "red letter" scriptures and extra-biblical sources.

## MCP Servers Installed

### 1. studybible-mcp ⭐ PRIMARY RESOURCE
**Location:** `~/.claude/mcp-servers/studybible-mcp/`
**Status:** ✅ Installed and configured

**Capabilities:**
- **18 tools** for comprehensive bible study
- **All 31,280 verses** with original Greek and Hebrew texts
- **Morphological parsing** for every verse
- **3 Lexicons:**
  - Liddell-Scott-Jones Greek (10,846 entries)
  - Abbott-Smith NT Greek (5,896 entries)
  - Brown-Driver-Briggs Hebrew (8,090 entries)
- **Commentaries:** 66 books of verse-level scholarly notes
- **Cross-References:** 22 thematic references + semantic similarity
- **Study Materials:**
  - Tyndale Bible Dictionary (500+ articles)
  - unfoldingWord Translation Notes
  - 200+ theological terms
  - 87 Ancient Near East cultural context entries
- **Graph Knowledge:** Genealogies, person events, place history

**Tools Available:**
1. Verse lookup
2. Word study
3. Lexicon search
4. Cross-references
5. Morphology parsing
6. Study notes
7. Bible dictionary
8. Theological terms
9. Graph knowledge
10. Ancient Near East context
11-18. Additional specialized tools

---

### 2. TheologAI
**Location:** `~/.claude/mcp-servers/TheologAI/`
**Status:** ✅ Installed and configured

**Capabilities:**
- **8 Translations:** ESV, NET, KJV, WEB, BSB, ASV, YLT, DBY
- **6 Public Domain Commentaries:**
  - Matthew Henry's Commentary
  - Jamieson-Fausset-Brown
  - Adam Clarke's Commentary
  - John Gill's Exposition
  - Keil-Delitzsch OT Commentary
  - Tyndale Bible Commentary
- **Cross-References:** Treasury of Scripture Knowledge
- **Historical Documents:** 18 documents (4 creeds, 8 confessions, 6 catechisms)
- **Language Tools:**
  - Strong's Concordance (14,298 entries)
  - STEPBible morphology (447,789 words)
- **Classic Texts:** 1000+ CCEL works

**Tools Available:**
- `bible_lookup` - Retrieve verses from multiple translations
- `commentary_lookup` - Access 6 commentaries
- `classic_text_lookup` - Search Christian classics
- `original_language_lookup` - Greek/Hebrew analysis
- `bible_verse_morphology` - Word-by-word parsing
- `bible_cross_references` - Related passages

---

## Configuration

The MCP servers are configured in `.mcp.json` in this directory. **You'll need to restart Claude Code** or start a new session for the MCPs to be loaded.

---

## Research Methodology

### Phase 1: Canonical Gospels (Red Letters)
Extract all direct quotes of Jesus from:
- **Matthew** - Sermon on the Mount, parables, teachings
- **Mark** - Actions and brief sayings
- **Luke** - Parables unique to Luke, teachings
- **John** - "I AM" statements, farewell discourse

### Phase 2: Acts and Epistles
Jesus's words recorded after resurrection:
- **Acts 1:4-8** - Final commission
- **Acts 9:4-6, 22:7-10, 26:14-18** - Paul's Damascus road experience
- **Revelation 1-3** - Letters to seven churches
- **Revelation 22:16-20** - Final words

### Phase 3: Original Language Analysis
For each saying:
- Greek text from original manuscripts
- Hebrew/Aramaic reconstructions where applicable
- Morphological parsing
- Lexical definitions
- Cultural context

### Phase 4: Cross-References and Context
- Old Testament prophecies fulfilled
- Thematic connections
- Historical/cultural background
- Ancient Near East parallels

### Phase 5: Commentaries and Interpretation
- Historical interpretations (Matthew Henry, etc.)
- Modern scholarly perspectives
- Alternative readings
- Textual variants

### Phase 6: Extra-Biblical Sources
Research non-canonical sources:
- **Gospel of Thomas** - 114 sayings attributed to Jesus
- **Papyrus Oxyrhynchus** - Early Jesus sayings fragments
- **Josephus** - Testimonium Flavianum
- **Talmudic references** - Historical mentions
- **Early Church Fathers** - Oral tradition quotes
- **Apocryphal gospels** - Infancy Gospel of Thomas, Gospel of Peter, etc.

---

## How to Use the MCPs

### Example Queries

**1. Get all Jesus's words from Matthew 5-7 (Sermon on the Mount):**
```
Using the studybible MCP, retrieve Matthew 5:1-7:29 and extract all red letter text (Jesus's direct quotes).
```

**2. Deep word study on "I AM" statements:**
```
Using studybible MCP's lexicon tools, analyze the Greek "ego eimi" (ἐγώ εἰμι) in John 8:58 with morphology and theological significance.
```

**3. Compare translations of a key teaching:**
```
Using TheologAI, show me John 3:16 in all 8 available translations side-by-side.
```

**4. Get commentary on a parable:**
```
Using TheologAI, show me Matthew Henry's and John Gill's commentaries on the Parable of the Sower (Matthew 13:1-23).
```

**5. Find all cross-references:**
```
Using studybible MCP, find all cross-references for Jesus's teaching on loving your enemies (Matthew 5:44).
```

**6. Ancient context:**
```
Using studybible MCP, what Ancient Near East cultural context helps understand the Parable of the Prodigal Son?
```

---

## Database Schema (Proposed)

### Table: `jesus_sayings`
```sql
CREATE TABLE jesus_sayings (
    id INTEGER PRIMARY KEY,
    reference TEXT NOT NULL,          -- e.g., "Matthew 5:3-12"
    text_english TEXT NOT NULL,       -- English translation
    text_greek TEXT,                  -- Original Greek if NT
    text_aramaic TEXT,                -- Reconstructed Aramaic if known
    context TEXT,                     -- Situation/audience
    theme TEXT,                       -- Main theme/topic
    canonical BOOLEAN DEFAULT TRUE,   -- Is this in canon?
    source TEXT NOT NULL,             -- Gospel or other source
    cross_refs TEXT,                  -- JSON array of references
    date_spoken TEXT,                 -- Approximate date if known
    location TEXT                     -- Where it was said
);
```

### Table: `word_studies`
```sql
CREATE TABLE word_studies (
    id INTEGER PRIMARY KEY,
    saying_id INTEGER REFERENCES jesus_sayings(id),
    greek_word TEXT,
    strongs_number TEXT,
    morphology TEXT,
    lexicon_definition TEXT,
    theological_significance TEXT
);
```

### Table: `commentaries`
```sql
CREATE TABLE commentaries (
    id INTEGER PRIMARY KEY,
    saying_id INTEGER REFERENCES jesus_sayings(id),
    commentator TEXT,              -- e.g., "Matthew Henry"
    commentary_text TEXT,
    year INTEGER,
    tradition TEXT                 -- Catholic, Protestant, Orthodox, etc.
);
```

---

## Sample Workflow

1. **Start a new Claude session** (to load the MCPs)

2. **Extract canonical sayings:**
   ```
   Using studybible MCP, extract all red letter text from Matthew chapter 5.
   For each saying, provide:
   - English text
   - Greek original
   - Verse reference
   - Immediate context
   ```

3. **Analyze key words:**
   ```
   For the word "blessed" (makarios/μακάριος) in the Beatitudes,
   use studybible lexicon tools to show:
   - All Greek forms
   - Lexicon entries
   - OT usage parallels
   ```

4. **Compare translations:**
   ```
   Using TheologAI, show Matthew 5:3-12 in KJV, ESV, and NET translations
   side-by-side to capture nuances.
   ```

5. **Get historical commentary:**
   ```
   Using TheologAI commentary_lookup, what did Matthew Henry say about
   the Beatitudes?
   ```

6. **Build comprehensive entry:**
   ```
   Create a complete database entry for Matthew 5:3 including:
   - All translation variants
   - Greek analysis
   - Cross-references
   - Commentary summary
   - Cultural context
   ```

---

## Additional Research Resources

### APIs (for later phases)
- **GetBible API** - 100+ translations (free, no auth)
  - https://getbible.net
  - Perfect for translation comparisons

- **Bible Brain API** - Audio bibles in 1,477 languages
  - https://4.dbt.io
  - Good for pronunciation research

### Datasets (for offline work)
- **scrollmapper/bible_databases** - 140 translations in 7 formats (MIT)
  - Can download for local SQLite queries
  - https://github.com/scrollmapper/bible_databases

- **Clear-Bible/macula-greek** - Scholarly Greek NT with syntax trees
  - Perfect for advanced linguistic analysis
  - https://github.com/Clear-Bible/macula-greek

### Extra-Biblical Sources to Research
1. **Gospel of Thomas** - Coptic text with 114 sayings
2. **Oxyrhynchus Papyri** - Early fragments (P.Oxy 1, 654, 655)
3. **Egerton Gospel** - Unknown gospel fragments
4. **Josephus** - Antiquities 18.3.3 (Testimonium Flavianum)
5. **Talmud references** - Sanhedrin 43a, etc.
6. **Quranic Jesus** - Islamic perspective on Isa (Jesus)
7. **Gnostic gospels** - Gospel of Philip, Gospel of Mary, etc.

---

## Next Steps

1. ✅ **MCPs installed and configured**
2. ⏳ **Restart Claude Code session** (to load MCPs)
3. ⏳ **Test MCP connectivity** - Try a simple verse lookup
4. ⏳ **Begin extraction** - Start with Matthew 5 (Sermon on Mount)
5. ⏳ **Set up database** - Create SQLite or PostgreSQL schema
6. ⏳ **Build extraction script** - Automate verse-by-verse processing
7. ⏳ **Research extra-biblical** - Source and verify non-canonical texts

---

## Notes

- The **studybible-mcp** is your primary tool - it has the most comprehensive features
- **TheologAI** is excellent for multiple translations and classic commentaries
- For **red letter text** specifically, you may need to use translation-specific tools (KJV and NKJV have red letters; Greek NT does not)
- Consider **thematic grouping**: Parables, "I AM" statements, Teachings on Kingdom, Ethics, Prophecy, etc.
- Extra-biblical research requires caution - document source reliability and scholarly consensus

---

## File Structure (Proposed)

```
/jesus-teachings-research/
├── data/
│   ├── canonical/
│   │   ├── matthew.json
│   │   ├── mark.json
│   │   ├── luke.json
│   │   └── john.json
│   ├── extra-biblical/
│   │   ├── gospel-thomas.json
│   │   ├── papyrus-fragments.json
│   │   └── josephus.json
│   └── analysis/
│       ├── word-studies/
│       ├── cross-references/
│       └── commentaries/
├── database/
│   └── jesus-teachings.db
├── scripts/
│   ├── extract-verses.py
│   ├── analyze-greek.py
│   └── build-database.py
└── docs/
    ├── methodology.md
    ├── sources.md
    └── findings.md
```

---

**Ready to begin!** Restart your Claude Code session to load the MCPs, then start querying the bible servers.
