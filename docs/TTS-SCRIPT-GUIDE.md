# TTS-Safe Script Writing Instructions

## Purpose
You are writing scripts that will be spoken aloud by an AI text-to-speech avatar. Your text is the ONLY input the TTS engine receives — it has no common sense, no context, and no judgment. Every ambiguity in your text WILL become an audible mistake. Write exactly what should be heard.

---

## 1. DATES — Always Write Them Out Fully

TTS engines routinely mangle dates. Never use numeric date formats.

| ❌ Never Write | ✅ Always Write |
|---|---|
| 2/26/2026 | February twenty-sixth, two thousand twenty-six |
| 2026 (as a year) | two thousand twenty-six |
| Feb 26 | February twenty-sixth |
| the 2020s | the twenty twenties |
| 1990s | nineteen nineties |
| 1800s | eighteen hundreds |
| 2000 (as a year) | the year two thousand |
| 03/15 | March fifteenth |

**Key rule:** Years in the 2000s should be "two thousand [and] twenty-six," NOT "twenty twenty-six." The latter often gets misread as two separate numbers. For the 1900s, use the natural spoken form: "nineteen ninety-nine."

---

## 2. NUMBERS — Spell Out or Hyphenate Everything

TTS engines don't know if "1,200" is "one thousand two hundred" or "twelve hundred." You decide.

| ❌ Never Write | ✅ Always Write |
|---|---|
| 15 | fifteen |
| 1,200 | twelve hundred (or one thousand two hundred) |
| 3.5 million | three-point-five million |
| $49.99 | forty-nine ninety-nine (or forty-nine dollars and ninety-nine cents) |
| 50% | fifty percent |
| #1 | number one |
| 1st, 2nd, 3rd | first, second, third |
| 300+ | more than three hundred |
| 10x | ten times |
| 24/7 | twenty-four seven |
| 1080p | ten-eighty p |
| 4K | four K |

**Large numbers:** Use the version a human would naturally say. "Three-point-two billion" is better than "three billion two hundred million."

**Ranges:** Write "between fifty and seventy-five" not "50–75." Dashes and en-dashes are invisible to TTS.

---

## 3. ABBREVIATIONS & ACRONYMS — Decide How It's Pronounced

TTS has to guess whether "Dr." is "doctor" or "drive." Don't make it guess.

| ❌ Never Write | ✅ Always Write |
|---|---|
| Dr. Smith | Doctor Smith |
| St. Louis | Saint Louis |
| Mr. / Mrs. / Ms. | Mister / Missus / Mizz |
| U.S. | the U.S. (or "the United States" if in a formal section) |
| AI | A.I. (spell with periods if you want each letter said) |
| CEO | C.E.O. |
| NASA | NASA (no periods — this one IS spoken as a word) |
| e.g. | for example |
| i.e. | that is |
| etc. | and so on |
| vs. | versus |
| approx. | approximately |
| govt | government |
| dept | department |
| Q1 | Q one (or first quarter) |
| Gen Z | Gen Zee |
| iOS | eye-oh-ess |
| API | A.P.I. |

**The rule:** If the acronym is spoken as a word (NASA, NATO, FOMO), write it as a word with no periods. If each letter is said individually (FBI, CEO, AI), either add periods between letters or spell it out entirely.

---

## 4. PUNCTUATION CONTROLS PACING — Use It Deliberately

Punctuation is your only tool for controlling rhythm, pauses, and emphasis. TTS treats punctuation as timing instructions.

**Commas** = short breath pause (~0.3s). Use them to prevent run-on phrasing:
- ❌ "The thing about this technology is that it changes everything"
- ✅ "The thing about this technology, is that it changes everything"

**Periods** = full stop pause (~0.6s). Break up long sentences. TTS handles two short sentences better than one long one.

**Ellipses (...)** = dramatic or trailing pause (~0.8–1s):
- "And then... it all made sense."

**Em dashes (—)** = abrupt pivot or interjection. Some TTS handles these well, others don't. Safer to restructure:
- ❌ "The results — and I'm not exaggerating — were incredible."
- ✅ "The results, and I'm not exaggerating, were incredible."

**Semicolons and colons** = avoid entirely. TTS either ignores them or produces awkward pauses. Rewrite as two sentences or use a comma.

**Exclamation marks** = use sparingly. One is fine for emphasis. Multiple (!!!) may cause the TTS to shout or glitch.

**Question marks** = essential. TTS uses these to apply rising intonation. If you omit them on a question, it'll sound like a statement.

---

## 5. CONTRACTIONS — Use Them, They Sound Human

Uncontracted speech is the single biggest tell that text was AI-generated. Humans almost never say "do not" in casual speech.

| ❌ Sounds Robotic | ✅ Sounds Natural |
|---|---|
| do not | don't |
| cannot | can't |
| it is | it's |
| they are | they're |
| would not | wouldn't |
| I will | I'll |
| we have | we've |
| that is | that's |
| let us | let's |
| is not | isn't |
| should not | shouldn't |
| could have | could've |
| I am | I'm |
| you are | you're |
| what is | what's |

**Exception:** When emphasis or formality is intentional: "I do NOT recommend this" — here the uncontracted form adds weight. Use this deliberately and rarely.

---

## 6. HOMOPHONES & AMBIGUOUS WORDS — Eliminate Confusion

Some words change pronunciation based on context. TTS can pick the wrong one.

| Word | Problem | Solution |
|---|---|---|
| read | "reed" vs. "red" | Use "read" only for present tense. Past tense: rewrite as "already went through it" or restructure. |
| lead | "leed" vs. "led" | Use "lead" for present/noun (the metal). Past tense: use "led." |
| live | "liv" vs. "lyve" | Clarify: "live broadcast" → "a live broadcast" (adjective is usually fine). "I live here" → usually fine. |
| close | "kloze" vs. "klohs" | "Close the door" vs. "close to home" — add context or restructure. |
| wound | "woond" vs. "wownd" | "wound up" vs. "a wound" — restructure if ambiguous. |
| bass | "base" vs. "bas" | Specify: "bass guitar" or "bass fish." |
| minute | "min-it" vs. "my-newt" | "A minute detail" → "a tiny detail." Time: "one minute" is fine. |
| resume | "re-zoom" vs. "rez-oo-may" | Use "résumé" with accents, or write "rez-oo-may" if TTS struggles. |
| content | "kon-TENT" vs. "KON-tent" | "Content creation" (noun) vs. "feeling content" (adjective) — usually fine from context. |
| project | "PRAH-ject" vs. "pruh-JECT" | "A project" (noun) vs. "to project" (verb) — restructure if ambiguous. |

---

## 7. SPECIAL CHARACTERS & SYMBOLS — Write the Words

TTS engines skip, mangle, or mispronounce most symbols.

| ❌ Symbol | ✅ Write Instead |
|---|---|
| & | and |
| @ | at |
| + | plus |
| = | equals |
| / (in text) | or, slash, per |
| < > | less than, greater than |
| ~ | approximately |
| ™ ® © | (omit entirely, or say "trademark" etc.) |
| → | leads to, becomes, then |
| • | (never use — these are visual-only) |

**URLs and emails:** Don't include raw URLs. Either omit them ("check the link in the description") or spell them out phonetically: "at example dot com."

**Hashtags:** Write "hashtag open A.I." not "#OpenAI."

---

## 8. FOREIGN WORDS & NAMES — Add Phonetic Hints

If a word isn't standard English, the TTS will mangle it.

**Strategy:** For uncommon names or foreign terms, include a phonetic respelling in parentheses the first time, or just write the phonetic version directly:

- ❌ "Nguyen" → ✅ "Win" (or "Noo-yen" depending on your preference)
- ❌ "Açaí" → ✅ "ah-sah-ee"
- ❌ "Huawei" → ✅ "Wah-way"
- ❌ "Shein" → ✅ "She-in"
- ❌ "GIF" → decide: "gif" (hard G) or "jif" and write it consistently

If you reference a company, person, or place with a non-obvious pronunciation, ALWAYS write the phonetic version. Do not assume the TTS engine knows how to pronounce proper nouns.

---

## 9. SENTENCE STRUCTURE — Short, Front-Loaded, Active

Long sentences cause TTS to lose natural rhythm and emphasis. The voice will sound flat and monotone over long clauses.

**Rules:**
- **Maximum two clauses per sentence.** If there's a third, break it out.
- **Front-load the point.** Put the key information at the start, not buried after a subordinate clause.
- **Use active voice.** "The team built this" not "This was built by the team."
- **Avoid nested parentheticals.** Anything you'd put in parentheses should be its own sentence.
- **One idea per sentence.** If you find "and" joining two unrelated thoughts, split them.

| ❌ Too Complex | ✅ Clean and Speakable |
|---|---|
| "The researchers, who had been working on this for over a decade at multiple institutions across the country, finally published their findings." | "The researchers had been working on this for over a decade. They finally published their findings." |
| "What we're seeing here is not just a minor update but rather a fundamental reimagining of how the entire system was designed to operate from the ground up." | "This isn't a minor update. It's a fundamental reimagining of how the entire system works." |

---

## 10. EMPHASIS & STRESS — Guide the TTS

If a word needs emphasis, you need to signal it since TTS can't read your mind.

**Methods:**
- **CAPS for single words:** "This is VERY important" — most TTS engines will add stress.
- **Italics** often don't translate to TTS. Don't rely on them.
- **Repetition:** "This changes things. It really changes things." Natural emphasis through structure.
- **Strategic comma before the key word:** "The answer is, no." (adds a beat of anticipation)

**Avoid:**
- ALL CAPS for full sentences (TTS may interpret as an acronym string)
- Bold or underline (invisible to TTS)
- Asterisks for emphasis (*really*) — TTS may read "asterisk"

---

## 11. LISTS & ENUMERATION — Convert to Flowing Speech

Bullet points and numbered lists are visual. They mean nothing to a voice.

| ❌ Written for Eyes | ✅ Written for Ears |
|---|---|
| "There are 3 reasons: 1) Cost 2) Speed 3) Quality" | "There are three reasons. First, cost. Second, speed. And third, quality." |
| "Features include: - Fast - Secure - Affordable" | "It's fast, secure, and affordable." |

**For longer lists (4+ items):** Group them. "On the technical side, it's fast, reliable, and secure. On the business side, it's affordable and scalable." Don't just rattle off more than three or four items in sequence — listeners lose track.

---

## 12. TRANSITIONS & FILLER — Sound Like a Person

Written transitions like "Furthermore" and "In conclusion" sound stiff when spoken. Use conversational bridges.

| ❌ Written Transition | ✅ Spoken Transition |
|---|---|
| Furthermore | And here's the thing |
| In addition | On top of that |
| However | But |
| In conclusion | So here's the bottom line |
| It is worth noting that | And this is worth calling out |
| Subsequently | After that |
| Nevertheless | Still |
| Consequently | So |
| As previously mentioned | Like I said |
| In the context of | When it comes to |
| It should be noted | Here's what matters |

---

## 13. COMMON TTS TRAPS — Specific Gotchas

These are patterns that reliably cause problems:

- **"2:30 PM"** → "two thirty in the afternoon"
- **"5'11""** → "five foot eleven"
- **"100°F"** → "a hundred degrees Fahrenheit"
- **"80s music"** → "eighties music"
- **"Wi-Fi"** → "Why-Fye" (usually fine, but test your TTS)
- **"PhD"** → "P.H.D." (add periods)
- **"9/11"** → "nine eleven"
- **"catch-22"** → "catch twenty-two"
- **"20/20 vision"** → "twenty-twenty vision"
- **"Gen AI"** → "generative A.I." (spell it out — "Gen AI" can sound like "Jenny")
- **"co-founder"** → "co-founder" (hyphen is fine here, TTS handles it)
- **"re-enter"** → "re-enter" (hyphen prevents "reenter" being said wrong)
- **"multi-step"** → just write "multi-step" (hyphen helps TTS)
- **Parenthetical citations like "(Smith, 2024)"** → omit entirely for spoken content

---

## 14. PRE-FLIGHT CHECKLIST

Before delivering any script, mentally run through this checklist:

1. **Read every sentence aloud in your head.** Does it sound like something a person would actually say?
2. **Are all numbers spelled out?** Including years, prices, percentages, and ordinals.
3. **Are all abbreviations expanded?** Dr., St., vs., etc.
4. **Are contractions used wherever natural?** "Do not" → "don't" unless emphasis is intended.
5. **Is every sentence two clauses or fewer?**
6. **Are there any symbols that should be words?** &, @, #, /, etc.
7. **Are any words ambiguous in pronunciation?** lead/lead, read/read, live/live.
8. **Are foreign names or uncommon words written phonetically?**
9. **Are lists converted to flowing speech?**
10. **Does the pacing feel right?** Enough commas for breath, short sentences for punch, periods for full stops.

---

## EXAMPLE: Before & After

### ❌ Before (written for reading):
"On 2/26/2026, Dr. Sarah Chen — CEO of NovaTech Inc. — announced that the company's Q4 revenue hit $3.2B, a 47% increase YoY. The AI-powered platform, which serves 10M+ users across 50+ countries, is expected to IPO in H1 2027."

### ✅ After (written for speaking):
"On February twenty-sixth, two thousand twenty-six, Doctor Sarah Chen, the C.E.O. of NovaTech, announced some big numbers. The company's fourth-quarter revenue hit three-point-two billion dollars. That's a forty-seven percent increase year over year. Their A.I.-powered platform now serves more than ten million users across over fifty countries. And they're expected to go public in the first half of two thousand twenty-seven."
