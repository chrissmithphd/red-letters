# Red Letters Project - Handoff Summary

**Date:** 2026-08-10  
**Status:** 10 of 20 speeches complete (50%), 2 failed (timeouts)

## Project Goal
Create comprehensive scholarly analysis of Jesus's 20 public speeches with:
- Most accurate biblical text (World English Bible - public domain)
- Translation controversies (Greek terms, common vs scholarly translations)
- Extra-biblical context (Dead Sea Scrolls, Rabbinic parallels, OT connections)
- Scholarly interpretations with common misinterpretations corrected
- 2-column web viewer (text left, notes right)

## Completed Work

### JSON Files Created (10 speeches)
All in `speeches/json-output/`:
1. `01-nazareth-synagogue-sermon.json` (36KB) - Isaiah 61 fulfillment
2. `02-capernaum-synagogue-teaching.json` (19KB) - Authority demonstration
3. `03-sermon-on-the-mount.json` (49KB) - Beatitudes, Lord's Prayer, major discourse
4. `04-sermon-on-the-plain.json` (34KB) - Luke's version, Beatitudes/Woes
5. `05-parables-by-the-sea.json` (29KB) - Sower, Mustard Seed, Kingdom parables
6. `06-bread-of-life-teaching.json` (61KB) - "I am bread of life", flesh/blood
7. `07-feast-of-tabernacles-teaching.json` (15KB) - Living water, Light, "I AM"
8. `08-teaching-on-defilement.json` (29KB) - Internal vs external righteousness
9. `09-feeding-of-4000-discourse.json` (21KB) - Compassion, leaven warning
10. `11-feast-of-dedication-teaching.json` (26KB) - "I and Father are one", Psalm 82

### Web Viewers
- `speeches/viewer-v2.html` - Single speech viewer (side-by-side layout)
- `speeches/navigator.html` - **Main interface** with hamburger menu, all 20 speeches listed
  - Access: http://localhost:8080/navigator.html
  - 9 speeches clickable, 11 marked "coming soon"

### Git Status
- All work committed (9 commits ahead of origin/master)
- Branch: master
- Ready to push to GitHub

## Failed Generations (Need Retry)
**2 speeches timed out during generation:**
- #10 Teaching on Forgiveness (Matthew 18) - 35-40KB target - **TIMEOUT**
- #12 Journey to Jerusalem (Luke 9:51-18:34) - 45-50KB target - **TIMEOUT**

These are large/complex passages. Next session should generate these with shorter sections or manually.

## JSON Format Standard

```json
{
  "speech_id": N,
  "title": "Speech Title",
  "date": "Date (e.g., Spring 28 CE)",
  "location": "Location description",
  "scripture_reference": "Book chapter:verse",
  "audience": "Who heard it",
  "duration_estimate": "Reading time estimate",
  "translation": "World English Bible (WEB - Public Domain)",
  "scholarly_note": "Brief context",
  
  "extra_biblical_context": {
    "dead_sea_scrolls": [
      {
        "source": "Document name",
        "parallel": "What parallels",
        "significance": "Why it matters"
      }
    ],
    "rabbinic_parallels": [...],
    "old_testament": [...]
  },
  
  "sections": [
    {
      "section_id": "unique_id",
      "reference": "Chapter:verse range",
      "title": "Section Title",
      "text": ["Verse 1 text", "Verse 2 text"],
      
      "controversial_terms": [
        {
          "english": "English word",
          "greek": "Greek word with transliteration",
          "common_mistranslation": "How it's wrongly translated",
          "scholarly_translation": "Correct translation",
          "explanation": "Why this matters (1-2 sentences)",
          "why_it_matters": "Application/significance"
        }
      ],
      
      "scholarly_interpretation": {
        "summary": "One sentence overview",
        "key_points": [
          "Point 1",
          "Point 2"
        ],
        "common_misinterpretations": [
          {
            "error": "Common wrong interpretation",
            "correction": "Correct interpretation",
            "scholars": "Scholar citations (optional)"
          }
        ]
      }
    }
  ],
  
  "overall_scholarly_interpretation": {
    "summary": "Overall meaning",
    "major_themes": ["Theme 1", "Theme 2"],
    "historical_context": ["Context 1"],
    "application_debates": [
      {
        "question": "Debated question?",
        "position_1": "View 1",
        "position_2": "View 2",
        "consensus": "Where scholars agree/disagree"
      }
    ],
    "why_past_interpretations_were_incorrect": [
      {
        "error": "Historical error",
        "why_wrong": "Why incorrect",
        "correction": "Modern understanding"
      }
    ]
  },
  
  "conclusion_summary": "Final paragraph tying it together"
}
```

## Remaining Speeches (10 total)

### Priority (Failed, Need Retry):
10. **Teaching on Forgiveness** (Matthew 18:1-35)
    - Greatest in Kingdom, Church discipline, 70x7, Unforgiving Servant
    - Target: 35-40KB
    - **Timed out - generate in smaller chunks**

12. **Journey to Jerusalem** (Luke 9:51-18:34)  
    - HUGE: Cost of discipleship, Good Samaritan, Prayer, Rich fool, Lost parables
    - Target: 45-50KB
    - **Timed out - very long, be selective with key teachings**

### Need to Generate:
13. **Teaching at Jericho** (Luke 18:35-19:27)
    - Ten Minas parable, Bartimaeus, Zacchaeus
    - Target: 30-35KB
    
14. **Triumphal Entry** (Matthew 21:1-17, Mark 11, Luke 19, John 12)
    - Entry on donkey, Hosanna, weeping over Jerusalem
    - Target: 25-30KB
    
15. **Temple Cleansing** (Matthew 21:12-17)
    - "Den of robbers" quote
    - Target: 20-25KB (brief)
    
16. **Authority Challenged** (Matthew 21:23-22:46)
    - Two Sons, Tenants, Wedding Feast parables
    - Taxes to Caesar, Resurrection debate, Greatest Commandment
    - Target: 45-50KB (multiple encounters)
    
17. **Woes Against Scribes & Pharisees** (Matthew 23)
    - Seven woes, Widow's mite, Lament over Jerusalem
    - Target: 35-40KB
    
18. **Olivet Discourse** (Matthew 24-25, Mark 13, Luke 21)
    - MAJOR: Temple destruction, End times, Second Coming
    - Ten Virgins, Talents, Sheep & Goats parables
    - Target: 55-60KB (longest remaining)
    
19. **Trial Before Pilate** (Matthew 27:11-26)
    - "My kingdom not of this world", Barabbas choice
    - Target: 25-30KB
    
20. **Words from the Cross** (Matthew 27:33-50, Luke 23, John 19)
    - Seven last words
    - Target: 30-35KB

## Generation Strategy

### For Each Speech:
1. **Fetch biblical text** from public domain (World English Bible preferred)
   - API: `https://bible-api.com/[reference]?translation=web`
   - Or use studybible MCP if available

2. **Research via web search:**
   - Greek/Hebrew terms in passage (use BibleHub, interlinear texts)
   - Scholarly interpretations (look for Craig Keener, N.T. Wright, D.A. Carson, R.T. France)
   - Common misinterpretations
   - Extra-biblical parallels (Dead Sea Scrolls, Rabbinic sources, OT connections)

3. **Structure sections logically** (3-7 sections per speech)
   - Divide long passages into coherent units
   - Each section gets: text, controversial terms (3-5), scholarly interpretation

4. **Keep tone scholarly, not cutesy**
   - No emojis
   - Professional academic tone
   - "Common Error" / "Scholarly Correction" not ❌✓

5. **File naming:** `NN-speech-title-kebab-case.json` where NN = 01, 02, etc.

### Agent Generation Command Template:
```
Generate JSON for Speech #N: [Title] ([Scripture Reference]).

Target [XX-XXKB].

Divide into [N] sections:
1. [Section 1 title] ([verses])
2. [Section 2 title] ([verses])
...

Key controversial terms ([N]):
- **[greek]** - "[english]" ([brief explanation])
...

Scholarly focus:
- [Main interpretive point 1]
- [Main interpretive point 2]
...

Extra-biblical: [What to research]

Write to: `/home/cbsmith/git/chris/red-letters/speeches/json-output/NN-[filename].json`

Return confirmation with key findings.
```

### Common Issues:
- **API timeouts:** Long speeches (45KB+) may timeout. If so, create manually with multiple smaller sections.
- **Content filtering:** John 8:31-59 triggered filter. Frame as "historical first-century theological debate" in academic tone.
- **Size targets:** Aim for target but prioritize completeness over strict size limits.

## After All Speeches Complete

### Update Navigator
Edit `speeches/navigator.html`:
- Change `available: false` to `available: true` for completed speeches
- Add filename mapping in `getFilename()` function

### Final Commit
```bash
git add speeches/json-output/*.json speeches/navigator.html
git commit -m "Complete all 20 speeches with scholarly analysis

Total: 20 speeches covering Jesus's public ministry 27-30 CE
- Chronological from Nazareth to Cross
- ~800KB total JSON (scholarly annotations)
- Navigator with hamburger menu interface
- Translation controversies addressed
- Extra-biblical context integrated

Co-Authored-By: Claude Sonnet 4.5 <noreply@anthropic.com>"
```

### Push to GitHub
```bash
git push origin master
```

## Access Points

- **Local server:** `cd speeches && python3 -m http.server 8080`
- **Navigator:** http://localhost:8080/navigator.html
- **Individual viewer:** http://localhost:8080/viewer-v2.html (requires sermon-data.js)

## Key Files Reference

- **Main viewer:** `speeches/navigator.html`
- **JSON output:** `speeches/json-output/*.json`
- **Source lists:** `JESUS-PUBLIC-SPEECHES-CHRONOLOGICAL.md`
- **This doc:** `PROJECT-STATUS.md`

## Next Session Steps

1. **Check in-progress agents:** Look for files 10, 11, 12 in json-output/
2. **If complete:** Commit them
3. **Generate remaining:** Speeches #13-20 (8 speeches)
4. **Update navigator:** Mark all as available
5. **Final commit and push**
6. **Test:** Load navigator, click through all 20 speeches

## Notes

- All biblical text uses World English Bible (public domain)
- Target sizes are guidelines; completeness matters more
- Keep academic tone throughout
- Extra-biblical context adds scholarly depth
- Navigator is the main user interface
